<template>
  <div id="app">
  <MainArticle></MainArticle>
  </div>
</template>

<script>
import MainArticle from "./components/MainArticle.vue";
import data from "./assets/data.json";

export default {
  name: "app",
  components: {
    MainArticle,
  },
  data() {
    return {
      articles: data,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
