<script setup>
import LineIcon from "../../Icons/LineIcon.vue";
</script>

<template>
  <section class="hero">
    <div class="container">
      <div class="hero__header">
        <p class="title__text">OUR MENU</p>
        <LineIcon />
      </div>
      <div class="hero__info">
        <h1 class="heading heading-1">Discover Our menu Chart</h1>
        <p class="text">
          Through True Rich Attended does no end it his mother since favourable
          real had half every him case in packages enquire we up ecstatic..
          Through True Rich Attended does no end it his mother
        </p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero {
  &__header {
    display: flex;
    gap: 1rem;
    align-items: center;
  }
  &__info {
    margin-top: 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    h1 {
      max-width: 33%;
    }
    p {
      max-width: 40%;
    }
  }
}
</style>
