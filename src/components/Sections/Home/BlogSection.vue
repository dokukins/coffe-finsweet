<script setup>
import BlogItem from "./BlogItem.vue";

const blogs = [
  {
    title: "Extra Thick Homemad Pizza Sauce",
    subtitle:
      "It is a long established fact that a reader will be distracted by the readable content of a page.",
    date: new Date(),
    image: "/src/assets/blog_image_1.png",
  },
  {
    title: "The Best Way to Store Fresh Herbs",
    subtitle:
      "It is a long established fact that a reader will be distracted by the readable content of a page.",
    date: new Date(),
    image: "/src/assets/blog_image_2.png",
  },
  {
    title: "5 ways to prepare porridge",
    subtitle:
      "It is a long established fact that a reader will be distracted by the readable content of a page.",
    date: new Date(),
    image: "/src/assets/blog_image_3.png",
  },
];
</script>
<template>
  <section class="blog">
    <div class="container">
      <h1 class="heading heading-1 blog__title">Read Our Lastest Blog</h1>
      <div class="blog__items">
        <BlogItem
          v-for="(blog, i) in blogs"
          :key="i"
          :title="blog.title"
          :subtitle="blog.subtitle"
          :date="blog.date"
          :image="blog.image"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.blog {
  margin-top: 10rem;
  &__title {
    margin-bottom: 4rem;
  }
  &__items {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: 1fr;
    gap: 2rem;
  }
}
</style>
