<template>
  <button class="btn">
    <slot></slot>
    <ArrowIcon color="#000000" />
  </button>
</template>

<script setup>
import ArrowIcon from "../Icons/ArrowIcon.vue";
</script>

<style lang="scss" scoped></style>
