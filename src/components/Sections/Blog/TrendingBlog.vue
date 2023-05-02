<script setup>
import ArrowIcon from "../../Icons/ArrowIcon.vue";
import PersonItem from "../PersonItem.vue";
</script>
<template>
  <div class="trend">
    <h2 class="heading heading-1">A guide to Thai Curry</h2>
    <div class="trend__footer">
      <PersonItem />
      <RouterLink to="/">
        <div class="read-more">
          Read More
          <span>
            <ArrowIcon color="#ffffff" />
          </span>
        </div>
      </RouterLink>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.trend {
  width: 50%;
  padding: 14rem 4rem 2.5rem 4rem;
  background: url("/src/assets/trending_blog_image.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: relative;
  &::before {
    content: "TRENDING";
    position: absolute;
    top: 0;
    left: 0;
    background: rgba($color: #ffc492, $alpha: 0.47);
    color: $primary;
    padding: 1rem 2rem;
  }
  &__footer {
    margin-top: 2.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
