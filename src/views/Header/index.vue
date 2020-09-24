<template>
  <div class="wrapper">
    <div class="container">
      <img src="@/assets/images/logo.a7995ad.svg" alt="" />
      <ul class="bar">
        <li
          :class="{ 'bar-item': true, 'bar-active': currentIndex === index }"
          v-for="(list, index) in barList"
          @click="change(index)"
          v-bind:key="list"
        >
          {{ list.barItem }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      currentIndex: 0,
      barList: [
        { id: 1, barItem: "首页" },
        { id: 2, barItem: "沸点" },
        { id: 3, barItem: "话题" },
        { id: 4, barItem: "小册" },
        { id: 5, barItem: "活动" }
      ]
    };
  },
  methods: {
    change: function(index) {
      this.currentIndex = index;
    }
  }
};
</script>

<style scoped lang="scss">
.wrapper {
  position: fixed;
  top: 0;
  height: 60px;
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: #fff;
  border-bottom: 1px solid rgba(244, 245, 245, 0.9);
  overflow: hidden;
  box-sizing: border-box;
  z-index: 9;
}

.container {
  width: 960px;
  line-height: 60px;
  display: flex;
  align-items: center;
}
.container img {
  margin-right: 24px;
}

.bar {
  margin: 0;
  padding: 0;
  display: flex;
}
.bar-item {
  list-style: none;
  cursor: pointer;
  color: #71777c;
  padding: 0 18px;
}
.bar-item:hover {
  color: #007fff;
}
.bar-active {
  color: #007fff;
}
</style>
