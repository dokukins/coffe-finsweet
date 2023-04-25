<template>
  <button class="btn">
    <slot></slot>
    <ArrowIcon />
  </button>
</template>

<script setup>
import ArrowIcon from "../Icons/ArrowIcon.vue";
</script>

<style lang="scss" scoped></style>
