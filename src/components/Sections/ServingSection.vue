<script setup>
import LineIcon from "../Icons/LineIcon.vue";
import ServeMenuItem from "./ServeMenuItem.vue";
import MenuIconCake from "../Icons/MenuIconCake.vue";

const subt =
  "Through True Rich Attended no end it his mother since favourable real had half every him.";
</script>

<template>
  <section class="serve">
    <div class="container">
      <div class="serve__header">
        <div class="title">
          <p class="title__text">WHAT WE ARE SERVING</p>
          <LineIcon />
        </div>
        <div class="serve__header__text">
          <h1 class="heading heading-1">
            We all have to eat, so why not do it beautifully?
          </h1>
          <p class="text">
            Through True Rich Attended does no end it his mother since
            favourable real had half every him case in packages enquire we up
            ecstatic. Through True Rich Attended does no end it his mother
          </p>
        </div>
      </div>
      <div class="serve__menu">
        <ServeMenuItem
          class="serve__menu__item"
          v-for="i in 6"
          :key="i"
          title="QUafe coffe"
          :subtitle="subt"
        >
          <div class="icon">
            <MenuIconCake />
          </div>
        </ServeMenuItem>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.serve {
  &__header {
    &__text {
      margin-top: 1.5rem;
      margin-bottom: 4rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 3.5rem;
      h1 {
        max-width: 55%;
      }
      p {
        max-width: 45%;
      }
    }
  }
  &__menu {
    background: $bg-grid;
    padding: 4rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8rem;
    &__item {
      position: relative;
      &:not(:nth-child(3n))::after {
        content: "";
        height: calc(8rem + 100%);
        width: 1px;
        position: absolute;
        top: calc(-4rem);
        right: -25%;
        background: gray;
      }
      .icon {
        width: 3rem;
        height: 3rem;
        border-radius: 50%;
        background: rgba($color: $bg-info, $alpha: 0.07);
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
  }
}
</style>
