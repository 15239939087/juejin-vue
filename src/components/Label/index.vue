<template>
  <div
    class="wrapper-label"
    :style="activeLabelStyle"
    @mouseover="showLabel"
    @mouseleave="hideLabel"
  ></div>
</template>

<script>
export default {
  name: "index",
  props: {
    activeLabelEleT: Number,
    activeLabelEleL: Number,
    isShowLabel: Boolean
  },
  data() {
    return {
      activeLabelStyle: {
        left: this.activeLabelEleL + "px",
        top: this.activeLabelEleT + 30 + "px"
      }
    };
  },
  methods: {
    showLabel: function() {
      this.$emit("listenToChildEvent", (this.isShowLabel = true));
    },
    hideLabel: function() {
      this.$emit("listenToChildEvent", (this.isShowLabel = false));
    }
  }
};
</script>

<style scoped lang="scss">
.wrapper-label {
  position: fixed;
  width: 300px;
  height: 150px;
  background-color: white;
  box-shadow: 1px 1px 13px rgba(0, 0, 0, 0.1);
  z-index: 10;
}
</style>
