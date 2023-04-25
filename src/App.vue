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

  <main class="main">
    <RouterView />
  </main>
</template>

<style scoped></style>
