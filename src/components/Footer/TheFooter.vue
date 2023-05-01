<template>
  <div class="footer__top">
    <RouterLink to="/" class="nav__logo">
      <img src="/src/assets/logo.svg" alt="" />
    </RouterLink>
    <ul class="links links-top">
      <li>
        <RouterLink to="/" class="link">Home</RouterLink>
      </li>
      <li>
        <RouterLink to="/about" class="link">Menu</RouterLink>
      </li>
      <li>
        <RouterLink to="/about" class="link">About Us</RouterLink>
      </li>
      <li>
        <RouterLink to="/about" class="link">Our Story</RouterLink>
      </li>
      <li>
        <RouterLink to="/about" class="link">Blog</RouterLink>
      </li>
      <li>
        <RouterLink to="/about" class="link">Contact</RouterLink>
      </li>
    </ul>
  </div>
  <div class="border">
    <div class="footer__bottom container">
      <p>© 2021 Finsweet | All rights reserved.</p>
      <ul class="links links-bottom">
        <li>
          <a href="#" class="link">
            <SocialIconFB />
          </a>
        </li>
        <li>
          <a href="#" class="link">
            <SocialIconTwitter />
          </a>
        </li>
        <li>
          <a href="#" class="link">
            <SocialIconInst />
          </a>
        </li>
        <li>
          <a href="#" class="link">
            <SocialIconLn />
          </a>
        </li>
      </ul>
      <RouterLink to="/about" class="side__link">
        Clone project <span><ArrowIcon color="#ffb577" /></span>
      </RouterLink>
    </div>
  </div>
</template>

<script setup>
import ArrowIcon from "../Icons/ArrowIcon.vue";
import SocialIconFB from "../Icons/SocialIconFB.vue";
import SocialIconInst from "../Icons/SocialIconInst.vue";
import SocialIconLn from "../Icons/SocialIconLn.vue";
import SocialIconTwitter from "../Icons/SocialIconTwitter.vue";
</script>

<style lang="scss" scoped>
.border {
  border-top: 1px solid rgba($color: white, $alpha: 0.06);
}
.footer {
  &__top {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 2.75rem;
    margin-bottom: 2rem;
  }
  &__bottom {
    padding: 1.5rem 0;
    display: flex;
    align-items: center;
    position: relative;
    p {
      position: absolute;
      left: 0;
    }
    ul {
      position: absolute;

      left: calc(50% - 132px / 2);
    }
    .side__link {
      position: absolute;
      right: 0;
    }
  }
}

.links {
  display: flex;

  color: $primary;
  &-top {
    gap: 2.5rem;
  }
  &-bottom {
    gap: 1.5rem;
  }
  .link {
    transition: all 0.2s;
    &:hover {
      color: $info;
    }
  }
}

.side__link {
  color: #fff;
  transition: all 0.2s;
  &:hover {
    color: $info;
  }
}
</style>
