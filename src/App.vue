<script setup>
import NavBar from "./components/Header/NavBar.vue";
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div class="container">
      <NavBar />
    </div>
  </header>

  <main>
    <RouterView />
  </main>
</template>

<style lang="scss">
@import "@/assets/styles/_variables.scss";
@import "@/assets/styles/global.scss";
@import "@/assets/styles/headings.scss";
</style>
