<template>
  <div class="home">
    <Header />
    <Nav />
    <Article />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/views/Header";
import Article from "@/views/Article";
import Nav from "@/views/Nav";

export default {
  name: "Home",
  components: {
    Header,
    Article,
    Nav
  }
};
</script>
