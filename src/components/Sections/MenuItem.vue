<script setup>
const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  price: {
    type: String,
    required: true,
  },
  image: {
    type: String,
    required: true,
  },
});

const getImage = () => {
  return `/src/assets/${props.image}`;
};
</script>
<template>
  <div class="menu__chart__item">
    <img :src="getImage()" alt="" />
    <div class="info">
      <p class="heading heading-2">{{ name }}</p>
      <p class="text text-2">{{ price }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.menu__chart__item {
  display: flex;
  flex-direction: column;
  .info {
    padding: 1.5rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #1f1d21;
  }
}
</style>
