<script setup>
import BaseButton from "../Base/BaseButton.vue";
</script>

<template>
  <section class="hero">
    <div class="container flex">
      <div class="hero__text">
        <div class="hero__main">
          <h1 class="heading heading-1">
            We serve high quality foods of all kinds.
          </h1>
          <p class="text">
            Edit this text to make it your own. To edit, simply click directly
            on the text to start adding your own words. You can move the text.
          </p>
          <RouterLink to="/about"
            ><BaseButton>View Menu</BaseButton></RouterLink
          >
        </div>
        <div class="hero__info">
          <div class="info__item">
            <h2 class="heading heading-2">Opening Times</h2>
            <p class="text">Sunday to Saturday | 09:00 AM to 11:00 PM</p>
          </div>
          <div class="info__item">
            <h2 class="heading heading-2">Location</h2>
            <p class="text">Master canteen, BBSR , Odisha 752054</p>
          </div>
          <div class="info__item">
            <h2 class="heading heading-2">Call us</h2>
            <p class="text">+9776462441</p>
          </div>
        </div>
      </div>
      <div class="hero__img">
        <img src="../../assets/header.png" alt="" />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.flex {
  gap: 2rem;
}
.hero {
  margin-top: 6rem;

  &__text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2.5rem;
  }
  &__main {
    h1 {
      color: $primary;
      margin-bottom: 1rem;
    }
    p {
      margin-bottom: 2rem;
    }
  }
  &__img {
    min-width: fit-content;
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
}
</style>
