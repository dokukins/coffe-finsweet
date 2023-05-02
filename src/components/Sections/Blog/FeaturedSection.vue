<template>
  <section class="featured">
    <h1 class="heading heading-1">Featured Blogs</h1>
    <div class="container">
      <TrendingBlog />
      <BlogList />
    </div>
  </section>
</template>

<script setup>
import TrendingBlog from "./TrendingBlog.vue";
import BlogList from "./BlogList.vue";
</script>

<style lang="scss" scoped>
.featured {
  margin-top: 6rem;

  .container {
    display: flex;
    gap: 2rem;
  }
  h1 {
    text-align: center;
    margin-bottom: 4rem;
  }
}
</style>
