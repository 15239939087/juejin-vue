<template>
  <div class="wrapper">
    <div class="main">
      <div class="left">
        <div class="content">
          <article class="article" v-for="art in articles" v-bind:key="art">
            <div class="desc">
              {{ art.name }} · {{ art.date }} · {{ art.label }}
            </div>
            <div class="title">{{ art.title }}</div>
            <div class="btn">
              <button class="support">210</button>
              <button class="comment">74</button>
            </div>
          </article>
        </div>
      </div>
      <div class="right">nav</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Article",
  data() {
    return {
      articles: [
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        },
        {
          name: "陈威",
          date: "17 天之前",
          label: "前端",
          title: "前端：写在30岁之前"
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
button {
  outline: none;
  border: none;
  background-color: #fff;
}
.wrapper {
  position: absolute;
  top: 106px;
  width: 100%;
  margin-top: 20px;
  font-family: sans-serif;
  display: flex;
  justify-content: center;
}
.main {
  width: 960px;
  height: 100%;
  display: flex;
  position: relative;
}
/*左侧内容板块*/
.left {
  background-color: #fff;
  width: 700px;
  overflow-x: hidden;
}
.content {
  height: 100%;
}
.article {
  height: 115px;
  padding: 18px 24px;
  box-sizing: border-box;
  border-bottom: 1px solid rgba(244, 245, 245, 0.9);
}
.article:hover {
  background-color: rgba(244, 245, 245, 0.5);
}
.desc {
  font-size: 12px;
  line-height: 15px;
  color: #b2bac2;
}
.title {
  height: 20px;
  margin: 6px 0 12px 0;
  font-weight: 600;
}
.btn {
}
.support {
  height: 24px;
  width: 62px;
  border: 1px solid rgba(244, 245, 245, 1);
  border-right: transparent;
}
.comment {
  height: 24px;
  width: 46px;
  border: 1px solid rgba(244, 245, 245, 1);
}

/*右侧内容板块*/
.right {
  background-color: #fff;
  width: 240px;
  position: absolute;
  right: 0;
}
@media (max-width: 960px) {
  .main {
    overflow-x: hidden;
  }
  .left {
    width: 960px;
  }
  .right {
    display: none;
  }
}
</style>
