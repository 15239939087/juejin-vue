<template>
  <div class="home">
    <Header />
    <Nav />
    <Article />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header";
import Article from "@/components/Article";
import Nav from "@/components/Nav";

export default {
  name: "Home",
  components: {
    Header,
    Article,
    Nav
  }
};
</script>
