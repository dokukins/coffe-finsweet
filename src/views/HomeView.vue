<script setup>
import BlogSection from "../components/Sections/Home/BlogSection.vue";
import HeroSection from "../components/Sections/Home/HeroSection.vue";
import KnowMoreSection from "../components/Sections/KnowMoreSection.vue";
import MenuSection from "../components/Sections/Home/MenuSection.vue";
import QuoteSection from "../components/Sections/Home/QuoteSection.vue";
import ServingSection from "../components/Sections/Home/ServingSection.vue";
import ContactSection from "../components/Sections/ContactSection.vue";
import BaseButton from "../components/Base/BaseButton.vue";

const images = ["know_more_1.png", "know_more_2.png"];
</script>

<template>
  <HeroSection />
  <KnowMoreSection :images="images">
    <template #button>
      <RouterLink to="/menu">
        <BaseButton>View Menu</BaseButton>
      </RouterLink>
    </template>
  </KnowMoreSection>
  <ServingSection />
  <MenuSection />
  <QuoteSection />
  <BlogSection />
  <ContactSection />
</template>

<style lang="scss"></style>
