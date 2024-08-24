<template>
  <div class="article-card">
    <img :src="article.image" alt="Article Image" />
    <h2>{{ article.title }}</h2><br>
    <p>{{ article.description }}</p><br>
    <button class="readArticles" @click="$emit('readArticle', article)">Читать статью</button>
  </div>
</template>

<script>
export default {
  props: {
    article: Object
  }
}
</script>

<style scoped>
.article-card {
  padding: 15px;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  height: auto;
  width: 30%;
}

.article-card img {
  width: 100%;
  height: 200px;
  border-radius: 8px;
}

.readArticles {
  background: rgb(209, 49, 49);
  color: #fafafa;
  border-radius: 4px;
  border: none;
  width: auto;
  margin: 5px;
  padding: 10px 20px;
  font-weight: 14px;
  float: right;
  cursor: pointer;
}

.readArticles:hover {
  background: rgb(78, 175, 14);
}
</style>
