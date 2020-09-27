<template>
  <div class="wrapper-label" :style="[left, top]">
    {{ activeLabelEleL }}{{ activeLabelEleT }}
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      left: {
        left: this.activeLabelEleL
      },
      top: {
        top: this.activeLabelEleT
      }
    };
  },
  props: {
    activeLabelEleT: Number,
    activeLabelEleL: Number
  }
};
</script>

<style scoped lang="scss">
.wrapper-label {
  position: absolute;
  top: 106px;
  left: 100px;
  width: 300px;
  height: 150px;
  background-color: green;
  z-index: 10;
}
</style>
