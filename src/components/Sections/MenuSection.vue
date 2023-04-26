<script setup>
import BaseButton from "../Base/BaseButton.vue";
import LineIcon from "../Icons/LineIcon.vue";
import MenuItem from "./MenuItem.vue";

const charts = [
  {
    name: "Drp Cofee",
    price: "$08.85",
  },
  {
    name: "Choco Cup Cake",
    price: "$4.85",
  },
  {
    name: "Chicken Burger",
    price: "$8.85",
  },
  {
    name: "French Fries",
    price: "$7.85",
  },
  {
    name: "Sandwitch",
    price: "$3.97",
  },
  {
    name: "Chinese Soup",
    price: "$8.85",
  },
];
</script>

<template>
  <section class="menu">
    <div class="container">
      <div class="menu__header">
        <div class="title">
          <p class="title__text">OUR MENU</p>
          <LineIcon />
        </div>
        <div class="menu__header__text">
          <h1 class="heading heading-1">Discover our menu chart</h1>
          <p class="text">
            Through True Rich Attended does no end it his mother since
            favourable real had half every him case in packages enquire we up
            ecstatic.. Through True Rich Attended does no end it his mother
          </p>
        </div>
        <div>
          <p
            :style="{ fontSize: '14px', color: '#c4e4ea', fontWeight: 'bold' }"
          >
            Most Popular Picks
          </p>
        </div>
      </div>
      <div class="menu__chart">
        <MenuItem
          v-for="(chart, i) in charts"
          :key="i"
          :name="chart.name"
          :price="chart.price"
          :image="`menu_image_${i + 1}.png`"
        />
      </div>
      <BaseButton>View Menu</BaseButton>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.menu {
  margin-top: 10rem;
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  &__header {
    margin-bottom: 5rem;
    &__text {
      margin-top: 1.5rem;
      margin-bottom: 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      p {
        max-width: 45%;
      }
    }
  }
  &__chart {
    margin-bottom: 2.5rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
}
</style>
