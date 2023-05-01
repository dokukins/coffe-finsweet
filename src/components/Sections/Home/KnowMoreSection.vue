<script setup>
import BaseButton from "../../Base/BaseButton.vue";
import HighlightIcon from "../../Icons/HighlightIcon.vue";
import LineIcon from "../../Icons/LineIcon.vue";
</script>

<template>
  <section class="know">
    <div class="container flex">
      <div class="know__text">
        <div class="title">
          <p class="title__text">KNOW MORE ABOUT US</p>
          <LineIcon />
        </div>
        <div class="know__main">
          <h1 class="heading heading-1">
            We source sustainable & line caught Foods
          </h1>
          <p class="text">
            Edit this text to make it your own. To edit, simply click directly
            on the text to start adding your own words. You can move the text by
            dragging and dropping the text anywhere on the page.
          </p>
        </div>

        <div class="know__info">
          <div class="info__item">
            <h2 class="heading-3">
              <HighlightIcon />
              10+ People
            </h2>
            <p class="text">We are Small Team</p>
            <p class="text">
              Through True Rich Attended does no end it his mother since
              favourable.
            </p>
          </div>
          <div class="info__item">
            <h2 class="heading-3">
              <HighlightIcon />
              2015
            </h2>
            <p class="text">We are Small Team</p>
            <p class="text">
              Through True Rich Attended does no end it his mother since
              favourable.
            </p>
          </div>
          <div class="info__item">
            <h2 class="heading-3">
              <HighlightIcon />
              200k
            </h2>
            <p class="text">We Served</p>
            <p class="text">
              Through True Rich Attended does no end it his mother since
              favourable.
            </p>
          </div>
        </div>

        <RouterLink to="/menu">
          <BaseButton>View Menu</BaseButton>
        </RouterLink>
      </div>

      <div class="know__img">
        <img
          class="img__item-bottom"
          src="/src/assets/know_more_1.png"
          alt=""
        />
        <img class="img__item-top" src="/src/assets/know_more_2.png" alt="" />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.flex {
  gap: 6rem;
}
.know {
  margin: 10rem 0;

  &__text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1.5rem;
  }

  &__main {
    h1 {
      margin-top: 1.5rem;
      margin-bottom: 2rem;
    }
  }

  &__info {
    display: flex;
    gap: 2rem;
  }

  .info__item p:nth-child(2) {
    margin-bottom: 1rem;
  }

  &__img {
    min-width: fit-content;
    display: flex;
    gap: 4rem;
  }

  .img__item {
    object-fit: contain;
    &-bottom {
      align-self: flex-end;
    }
    &-top {
      align-self: flex-start;
    }
  }
}
</style>
