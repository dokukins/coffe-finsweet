<template>
  <nav class="nav">
    <RouterLink to="/" class="nav__logo">
      <img src="../../assets/logo.svg" alt="" />
    </RouterLink>
    <ul class="menu">
      <li class="menu__list">
        <RouterLink to="/" class="menu__link">Home</RouterLink>
      </li>
      <li class="menu__list">
        <RouterLink to="/menu" class="menu__link">Menu</RouterLink>
      </li>
      <li class="menu__list">
        <RouterLink to="/about" class="menu__link">About Us</RouterLink>
      </li>
      <li class="menu__list">
        <RouterLink to="/story" class="menu__link">Our Story</RouterLink>
      </li>
      <li class="menu__list">
        <RouterLink to="/blog" class="menu__link">Blog</RouterLink>
      </li>
      <li class="menu__list">
        <RouterLink to="/contact" class="menu__link">Contact</RouterLink>
      </li>
    </ul>
    <RouterLink to="/about" class="side__link">
      Clone project <span><ArrowIcon color="#ffb577" /></span>
    </RouterLink>
  </nav>
</template>

<script setup>
import ArrowIcon from "../Icons/ArrowIcon.vue";
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  gap: 3rem;
  padding: 1.75rem 0;
}

.menu {
  display: flex;
  justify-self: flex-start;
  gap: 2.5rem;
  color: $primary;
  &__link {
    transition: all 0.2s;
    &:hover {
      color: $info;
    }
  }
}

.side__link {
  margin-left: auto;
  color: #fff;
  transition: all 0.2s;
  &:hover {
    color: $info;
  }
}
</style>
