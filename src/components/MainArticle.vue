<template>
        <h1 class="title-header"><span>Hello World, here is the news!</span></h1>
        <button v-on:="getArticleData">Click Here To View The News!</button>
        <div v-for="articleData in articleDataList" :key="articleData.title" class="article-data">
            <div class="article-image">
                <img :src=articleData.media>
            </div>
            <div class="article-info">
                <div class="background-color">
                    <span style="font-size: 30px">{{articleData.excerpt}}</span>
                </div>
                <p></p>
                <p></p>
                <div>
                    By: <span style="font-size: 22px">{{articleData.author}}</span>
                </div>
                <p></p>
                <h1 style="font-size: 10px"></h1>
                <h1 style="font-size: 15px"></h1>
                <div>
                    <span><em>{{articleData.summary}}</em></span>
                </div>
                <h1 style="font-size: 10px"></h1>
                <div>
                    <span><a href="{{articleData.link}}"> Read More...</a></span>
                </div>
            </div>
        </div>
  </template>

<style scoped>

.title-header {
    padding: 20px;
    align-items: center;
    font-style: italic;
}

.article-data {
  display: inline-flex;
  flex-direction: row-reverse;
  align-items: center;
  margin-top: 20px;
  margin-left: 20px;
  padding-left: 80px;
  padding-right: 80px;
  padding-bottom: 80px;
  line-height: 2em;
}

.article-data:nth-child(odd) {
  display: inline-flex;
  flex-direction: row;
  align-items: center;
  margin-top: 20px;
  margin-left: 20px;
  padding-left: 80px;
  padding-right: 80px;
}

.article-image {
  flex-grow: 1;
}

.background-color {
    background-color: yellow;
}

.article-info {
  flex-grow: 8;
  text-align: left;
  padding-left: 20px;
}

div img {
  width: 500px;
  height: auto;
  float:left;
  clear:left;
  padding-left: 15px;
  padding-right: 15px;
  border-radius: 30px;
}

button {
    padding:10px;
    background-color: #1aa832;
    color: white;
    border: 1px solid #ccc;
}

</style>

  
  <script>
  export default {
    name: 'MainArticle',
    data() {
        return {
            articleDataList: []
        };
    },
    methods: {
        getArticleData() {
            fetch("data.json")
            .then(response => response.json())
            .then(data => (this.articleDataList = data));
        }
    }
  };
  </script>
  
