<script setup>
import { ref, useSlots } from "vue";
import HighlightIcon from "../Icons/HighlightIcon.vue";
import LineIcon from "../Icons/LineIcon.vue";

const slots = useSlots();
const hasButton = ref(!!slots.button);

const props = defineProps({
  images: Array,
});
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

        <div class="know__info" :class="{ 'pb-5': !hasButton }">
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

        <slot name="button"></slot>
      </div>

      <div class="know__img">
        <img
          v-for="img in images"
          :key="img"
          :src="`/src/assets/${img}`"
          alt=""
        />
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
    img {
      object-fit: contain;
      &:first-child {
        align-self: flex-end;
      }
      &:last-child {
        align-self: flex-start;
      }
    }
  }
}
</style>
