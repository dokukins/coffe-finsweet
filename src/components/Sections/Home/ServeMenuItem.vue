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
});
</script>
<template>
  <div class="menu__item">
    <slot></slot>
    <h2 class="heading heading-4">{{ title }}</h2>
    <p class="text">{{ subtitle }}</p>
  </div>
</template>

<style lang="scss" scoped>
.menu__item {
  h2 {
    margin-top: 1.5rem;
    margin-bottom: 0.75rem;
  }
}
</style>
