<template>
  <div class="wrapper">
    <div class="container">
      <img class="logo" src="@/assets/images/logo.a7995ad.svg" alt="" />
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
      <ul class="operation">
        <li class="operation-item">
          <input class="search" type="text" placeholder="搜索掘金" />
        </li>
        <li class="operation-item"><button class="write">写文章</button></li>
        <li class="operation-ding">
          <img class="ding" src="@/assets/images/ding.png" alt="" />
        </li>
        <li class="operation-avatar">
          <img class="avatar" src="@/assets/images/avatar.jpg" alt="" />
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
  position: relative;
  width: 960px;
  line-height: 60px;
  display: flex;
  align-items: center;
}
.container .logo {
  margin-right: 24px;
}

.bar {
  margin: 0;
  padding: 0;
  display: flex;
}
.bar-item {
  list-style: none;
  white-space: nowrap;
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

.operation {
  display: flex;
  margin: 0;
  padding-left: 128px;
}
.operation li {
  list-style: none;
}
.operation-item {
  padding: 0px 14px;
}

.search {
  width: 148px;
  height: 28px;
  outline: none;
  border: 1px solid rgba(0, 0, 0, 0.2);
}
.search::-webkit-input-placeholder {
  color: #a1a7ac;
  padding-left: 12px;
}

.write {
  height: 32px;
  background-color: #007fff;
  padding: 0 12px;
  color: white;
  border: none;
  border-radius: 4px;
  outline: none;
  cursor: pointer;
  white-space: nowrap;
}
.write:hover {
  background-color: #0876e4;
}

.operation-ding {
  padding: 0px 14px;
}
.ding {
  width: 24px;
  height: 24px;
  vertical-align: middle;
}
.operation-avatar {
  margin-right: 0;
  padding-left: 14px;
}
.avatar {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  vertical-align: middle;
}
</style>
