<script setup>
defineProps({
  title: String,
  subtitle: String,
  image: String,
});
</script>
<template>
  <li class="blog__item">
    <RouterLink :to="`/blog/${title}`">
      <img :src="image" alt="" />
      <div class="blog__text">
        <p>{{ title }}</p>
        <p>
          {{ subtitle }}
        </p>
      </div>
    </RouterLink>
  </li>
</template>

<style lang="scss" scoped>
.blog {
  &__item a {
    display: flex;
    gap: 2rem;
  }
  &__text {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    justify-content: center;
    p {
      &:first-child {
        color: $primary;
      }
    }
  }
}
</style>
