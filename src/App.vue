<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import "@/styles/colors.scss";

body {
  margin: 0;
  padding: 0;
  background-color: rgba(244, 245, 245, 0.9);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $dark-blue;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
