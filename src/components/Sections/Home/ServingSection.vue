<script setup>
import LineIcon from "../../Icons/LineIcon.vue";
import ServeMenuItem from "./ServeMenuItem.vue";
import MenuIconCake from "../../Icons/MenuIconCake.vue";
import MenuIconCofee from "../../Icons/MenuIconCofee.vue";
import MenuIconFood from "../../Icons/MenuIconFood.vue";
import MenuIconGrill from "../../Icons/MenuIconCake.vue";
import MenuIconSnack from "../../Icons/MenuIconSnack.vue";
import MenuIconCocktail from "../../Icons/MenuIconCake.vue";

const serves = [
  {
    title: "Quafe Cake",
    subtitle:
      "Through True Rich Attended no end it his mother since favourable real had half every him.",
    icon: MenuIconCake,
  },
  {
    title: "Cofee",
    subtitle:
      "Through True Rich Attended no end it his mother since favourable real had half every him.",
    icon: MenuIconCofee,
  },
  {
    title: "Fast Food",
    subtitle:
      "Through True Rich Attended no end it his mother since favourable real had half every him.",
    icon: MenuIconFood,
  },
  {
    title: "Cocktails",
    subtitle:
      "Through True Rich Attended no end it his mother since favourable real had half every him.",
    icon: MenuIconCocktail,
  },
  {
    title: "Grill",
    subtitle:
      "Through True Rich Attended no end it his mother since favourable real had half every him.",
    icon: MenuIconGrill,
  },
  {
    title: "Snacks",
    subtitle:
      "Through True Rich Attended no end it his mother since favourable real had half every him.",
    icon: MenuIconSnack,
  },
];
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
          v-for="serve in serves"
          :key="serve.title"
          :title="serve.title"
          :subtitle="serve.subtitle"
        >
          <div class="icon">
            <component :is="serve.icon" />
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
        background: rgba($color: #fff, $alpha: 0.06);
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
