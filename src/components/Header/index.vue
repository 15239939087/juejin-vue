<template>
  <div class="wrapper">
    <div class="container">
      <img class="logo" src="@/assets/images/logo.a7995ad.svg" alt="" />
      <ul class="bar">
        <li
          :class="{ 'bar-item': true, 'bar-active': currentIndex === index }"
          v-for="(list, index) in barList"
          @click="change(index)"
          v-bind:key="index"
        >
          {{ list.barItem }}
        </li>
      </ul>
      <ul class="operation">
        <li class="operation-item">
          <div class="input">
            <input class="search control" type="text" placeholder="搜索掘金" />
            <label for="" class="input-label">搜索掘金</label>
          </div>
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
  padding-left: 108px;
}
.operation li {
  list-style: none;
}
.operation-item {
  padding: 0px 14px;
}


.input {
  position: relative;
  border-bottom: 1px solid #d0d0d5;
}


.search {
  width: 148px;
  height: 28px;
  outline: none;
  border: none;
  padding: 0 12px;
  color: #bbbbbb;
  /*border: 1px solid rgba(0, 0, 0, 0.2);*/
  border-bottom: 1px solid #d0d0d5;
}

.control {
  margin: 0;
  line-height: 1.5;
  outline: none;
}
.control:placeholder-shown::placeholder {
  color: transparent;
}
.input-label {
  position: absolute;
  font-size: 14px;
  line-height: 1.5;
  left: 16px;
  top: 20px;
  color: #a2a9b6;
  padding: 0 2px;
  transform-origin: 0 0;
  pointer-events: none;
  transition: all 0.25s;
}


/*.search::-webkit-input-placeholder {*/
/*  color: #2486ff;*/
/*  padding-left: 12px;*/
/*}*/


.control:not(:placeholder-shown) + .input-label,
.control:focus + .input-label {
  color: #2486ff;
  transform: scale(0.75) translate(-8px, -18px);
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
