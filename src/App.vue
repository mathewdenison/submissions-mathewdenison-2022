<template>
  <h1 class="title-header"><span>Hello World, here is the news!</span></h1>
  <component :is="getArticleData"> Click Here To View The News! </component>
  <div
    v-for="articleData in articleDataList"
    :key="articleData.title"
    class="article-data"
  >
    <div class="article-image">
      <img :src="articleData.media" />
    </div>
    <div class="article-info">
      <div class="background-color">
        <span style="font-size: 30px">{{ articleData.excerpt }}</span>
      </div>
      <p></p>
      <p></p>
      <div>
        By: <span style="font-size: 22px">{{ articleData.author }}</span>
      </div>
      <p></p>
      <h1 style="font-size: 10px"></h1>
      <h1 style="font-size: 15px"></h1>
      <div>
        <span
          ><em>{{ articleData.summary }}</em></span
        >
      </div>
      <h1 style="font-size: 10px"></h1>
      <div>
        <span><a href="{{articleData.link}}"> Read More...</a></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      articleDataList: [],
    };
  },
  methods: {
    getArticleData() {
      fetch("http://localhost:3000/articles")
        .then((response) => response.json())
        .then((data) => (this.articleDataList = data));
    },
  },
};
</script>

<style scoped src="@/components/MainArticle.vue">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
