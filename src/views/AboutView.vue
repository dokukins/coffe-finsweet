<script setup>
import HistorySection from "../components/Sections/About/HistorySection.vue";
import KnowMoreSection from "../components/Sections/KnowMoreSection.vue";
import ContactSection from "../components/Sections/ContactSection.vue";

const images = ["know_more_3.png", "know_more_4.png"];
</script>

<template>
  <KnowMoreSection :images="images"> </KnowMoreSection>
  <HistorySection />
  <ContactSection />
</template>

<style lang="scss"></style>
