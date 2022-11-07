<template>
    <div>
        <h1>Hello World, here is the news!</h1>
        <button v-on:click="getArticleData">Get Article Data</button>
        <div v-for="articleData in articleDataList" :key="articleData.title" class="article-data">
            <div class="article-image">
                <img :src=articleData.media>
            </div>
            <div class="article-info">
                <div>
                    <span>{{articleData.author}}</span>
                </div>
                <div>
                    <span>{{articleData.excerpt}}</span>
                </div>
                <div>
                    <span>{{articleData.summary}}</span>
                </div>
                <div>
                    <span><a href="url">{{articleData.link}}</a></span>
                </div>
            </div>
        </div>
    </div>
  </template>

<style scoped>
.article-data {
  display: flex;
  align-items: center;
  margin-top: 20px;
  margin-left: 20px;
  border-bottom: 2px solid #ccc;
  padding: 20px;
}

.article-image {
  flex-grow: 1;
}

.article-info {
  flex-grow: 8;
  text-align: left;
  padding-left: 20px;
}

img {
  width: 200px;
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
  
