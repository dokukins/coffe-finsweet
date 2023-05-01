<script setup>
import BaseRadioButton from "../../Base/BaseRadioButton.vue";
import MenuItem from "../MenuItem.vue";
import { ref, computed } from "vue";

const charts = [
  {
    name: "Drp Cofee",
    price: "$08.85",
    image: "menu_image_1.png",
    category: "cofee",
  },
  {
    name: "Choco Cup Cake",
    price: "$4.85",
    image: "menu_image_2.png",
    category: "quafecake",
  },
  {
    name: "Chicken Burger",
    price: "$8.85",
    image: "menu_image_3.png",
    category: "fastfood",
  },
  {
    name: "French Fries",
    price: "$7.85",
    image: "menu_image_4.png",
    category: "fastfood",
  },
  {
    name: "Sandwitch",
    price: "$3.97",
    image: "menu_image_5.png",
    category: "fastfood",
  },
  {
    name: "Chinese Soup",
    price: "$8.85",
    image: "menu_image_6.png",
    category: "fastfood",
  },
  {
    name: "Quafe Brade",
    price: "$08.85",
    image: "menu_image_7.png",
    category: "quafecake",
  },
  {
    name: "Dalgona Cofee",
    price: "$4.85",
    image: "menu_image_8.png",
    category: "cofee",
  },
  {
    name: "Chowmin Noodle",
    price: "$8.85",
    image: "menu_image_9.png",
    category: "fastfood",
  },
  {
    name: "Coka Cola",
    price: "$7.85",
    image: "menu_image_10.png",
    category: "cocktails",
  },
  {
    name: "Fruit Salad",
    price: "$3.97",
    image: "menu_image_11.png",
    category: "snacks",
  },
  {
    name: "Cocktail",
    price: "$8.85",
    image: "menu_image_12.png",
    category: "cocktails",
  },
];

const filters = [
  {
    id: "all",
    label: "All",
    value: "all",
  },
  {
    id: "fastfood",
    label: "Fast Food",
    value: "fastfood",
  },
  {
    id: "cofee",
    label: "Cofee",
    value: "cofee",
  },
  {
    id: "cocktails",
    label: "Cocktails",
    value: "cocktails",
  },
  {
    id: "quafecake",
    label: "Quafe Cake",
    value: "quafecake",
  },
  {
    id: "snacks",
    label: "Snacks",
    value: "snacks",
  },
];

const selectedRadio = ref("all");

const filteredCharts = computed(() => {
  return selectedRadio.value === "all"
    ? charts
    : charts.filter((c) => c.category === selectedRadio.value);
});
</script>

<template>
  <section class="menu">
    <div class="container">
      <div class="menu__filters">
        <BaseRadioButton
          v-for="filter in filters"
          :key="filter.id"
          :id="filter.id"
          :label="filter.label"
          :value="filter.value"
          v-model="selectedRadio"
        />
      </div>
      <div class="menu__list">
        <MenuItem
          v-for="(chart, i) in filteredCharts"
          :key="i"
          :name="chart.name"
          :price="chart.price"
          :image="chart.image"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.menu {
  margin-top: 9rem;
  &__filters {
    margin-bottom: 4rem;
    display: flex;
    gap: 1rem;
    font-size: 2rem;
    input {
      width: 2rem;
    }
  }

  &__list {
    margin-bottom: 2.5rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
}
</style>
