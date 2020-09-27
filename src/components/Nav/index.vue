<template>
  <div class="root">
    <div class="wrapper">
      <div class="nav">
        <div class="nav-item">
          <a
            :class="{ 'nav-cell': true, 'nav-active': currentIndex === index }"
            v-for="(nav, index) in navItems"
            v-bind:key="index"
            @click="change(index)"
            @mouseover="getPositionLabel(index)"
          >
            {{ nav.label }}</a
          >
        </div>
        <div class="nav-manage">标签管理</div>
      </div>
    </div>
    <Label
      activeLabelEleT="activeLabelEleT"
      activeLabelEleL="activeLabelEleL"
    />
  </div>
</template>

<script>
import Label from "@/components/Label/index.vue";
export default {
  name: "Nav",
  components: {
    Label
  },
  data() {
    return {
      currentIndex: 0,
      activeLabelEleT: 0,
      activeLabelEleL: 0,
      navItems: [
        {
          id: 1,
          label: "推荐"
        },
        {
          id: 2,
          label: "关注"
        },
        {
          id: 3,
          label: "后端"
        },
        {
          id: 4,
          label: "前端"
        },
        {
          id: 5,
          label: "Android"
        },
        {
          id: 6,
          label: "iOS"
        },
        {
          id: 7,
          label: "人工智能"
        },
        {
          id: 8,
          label: "开发工具"
        },
        {
          id: 9,
          label: "代码人生"
        },
        {
          id: 10,
          label: "阅读"
        }
      ]
    };
  },
  methods: {
    change: function(index) {
      this.currentIndex = index;
    },
    getPositionLabel: function(index) {
      let activeLabelEle = document.getElementsByClassName("nav-cell")[index];
      let activeLabelEleL = activeLabelEle.getBoundingClientRect().left;
      let activeLabelEleT = activeLabelEle.getBoundingClientRect().top;
      this.activeLabelEleT = activeLabelEleT;
      this.activeLabelEleL = activeLabelEleL;
    }
  }
};
</script>

<style scoped lang="scss">
.wrapper {
  position: fixed;
  top: 60px;
  height: 46px;
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: #fff;
  border-bottom: 1px solid rgba(244, 245, 245, 0.9);
  overflow: hidden;
  z-index: 9;
  box-sizing: border-box;
}
.nav {
  display: flex;
  width: 960px;
  flex-direction: row;
  font-size: 13px;
  line-height: 46px;
  justify-content: space-between;
}

.nav-item {
  text-align: center;
}

.nav-cell {
  padding: 0 12px;
  text-decoration: none;
  color: #bbbbbb;
  white-space: nowrap;
  cursor: pointer;
}
.nav-cell:hover {
  color: #007fff;
}
.nav-cell:nth-child(1) {
  padding-left: 0;
  text-align: left;
}
.nav-active {
  color: #007fff;
  cursor: default;
}

.nav-manage {
  color: #bbbbbb;
  cursor: pointer;
}
.nav-manage:hover {
  color: #007fff;
}
</style>
