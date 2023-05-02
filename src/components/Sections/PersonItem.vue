<template>
  <div class="person">
    <img src="/src/assets/person_image.png" alt="" />
    <div class="person__text">
      <p>Andrew Jonson</p>
      <p>27th January 2021</p>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.person {
  display: flex;
  gap: 1rem;

  img {
    height: fit-content;
  }
  &__text {
    p {
      &:first-child {
        color: $primary;
      }
    }
  }
}
</style>
