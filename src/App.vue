<script setup>
import TheFooter from "./components/Footer/TheFooter.vue";
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

  <footer style="margin: auto 0 0 0">
    <TheFooter />
  </footer>
</template>

<style lang="scss">
@import "@/assets/styles/_variables.scss";
@import "@/assets/styles/global.scss";
@import "@/assets/styles/headings.scss";
</style>
