<script setup>
import ArticleItem from "./ArticleItem.vue";

const articles = [
  {
    title: "A guide to Thai Curry",
    image: "/src/assets/article_image_1.png",
  },
  {
    title: "The best guacamole recipe with only 4 ingredients",
    image: "/src/assets/article_image_2.png",
  },
  {
    title: "How to store Tomatoes (and Whether to Refrigerate Them)",
    image: "/src/assets/article_image_3.png",
  },
  {
    title: "The Absolute Best Way to Cook French Fries",
    image: "/src/assets/article_image_4.png",
  },
];
</script>
<template>
  <section class="article">
    <h2 class="heading heading-4">All Articles</h2>
    <div class="container">
      <ul class="article__grid">
        <ArticleItem
          v-for="article in articles"
          :key="article.title"
          :title="article.title"
          :image="article.image"
        />
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.article {
  margin-top: 6rem;
  &__grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    row-gap: 2.5rem;
    column-gap: 1.5rem;
  }
  h2 {
    text-align: center;
    margin-bottom: 4rem;
  }
}
</style>
