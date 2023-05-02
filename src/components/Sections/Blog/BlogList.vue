<template>
  <ul class="featured__blogs">
    <BlogListItem
      v-for="blog in blogs"
      :key="blog.title"
      :title="blog.title"
      :subtitle="blog.subtitle"
      :image="blog.image"
    />
  </ul>
</template>

<script setup>
import BlogListItem from "./BlogListItem.vue";

const blogs = [
  {
    title: "You can move the text by dragging and dropping the text ",
    subtitle:
      "Writing UX copies can be a little frustrating and confusing, and sometimes ",
    image: "/src/assets/blog_item_1.png",
  },
  {
    title: "Edit this text to make it your own. To edit, simply ",
    subtitle:
      "Writing UX copies can be a little frustrating and confusing, and sometimes ",
    image: "/src/assets/blog_item_2.png",
  },
  {
    title: "You can move the text by dragging and dropping the text ",
    subtitle:
      "Writing UX copies can be a little frustrating and confusing, and sometimes ",
    image: "/src/assets/blog_item_3.png",
  },
];
</script>

<style lang="scss" scoped>
.featured {
  &__blogs {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
}
</style>
