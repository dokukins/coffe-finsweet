<template>
  <li class="article__grid__item">
    <img :src="image" alt="" />
    <div class="info">
      <PersonItem />
      <p>{{ title }}</p>
      <RouterLink :to="`/blog/${title}`">
        <div class="read-more">
          Read More
          <span>
            <ArrowIcon color="#ffffff" />
          </span>
        </div>
      </RouterLink>
    </div>
  </li>
</template>

<script setup>
import ArrowIcon from "../../Icons/ArrowIcon.vue";
import PersonItem from "../PersonItem.vue";

defineProps({
  title: String,
  image: String,
});
</script>

<style lang="scss" scoped>
.article__grid__item {
  display: flex;
  gap: 2.5rem;
  align-items: center;
}

.info {
  p {
    color: $primary;
    margin-top: 1.5rem;
    margin-bottom: 1.5rem;
  }
}
</style>
