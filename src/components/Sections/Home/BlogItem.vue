<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  subtitle: {
    type: String,
    required: true,
  },
  date: {
    type: Date,
    required: true,
  },
  image: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="blog__item">
    <div class="info">
      <p class="text">{{ date.toLocaleDateString() }}</p>
      <h3 class="heading heading-4">{{ title }}</h3>
      <p class="text">{{ subtitle }}</p>
    </div>
    <img :src="image" alt="" />
  </div>
</template>

<style lang="scss" scoped>
.blog__item {
  background: $bg-secondary;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.info {
  padding: 2rem;
  h3 {
    margin-top: 0.5rem;
    margin-bottom: 1rem;
  }
  & p:last-child {
    margin-bottom: 2rem;
  }
}
</style>
