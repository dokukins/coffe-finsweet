<template>
  <div class="map">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d193595.25280002074!2d-74.14448754461243!3d40.69763123334598!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24fa5d33f083b%3A0xc80b8f06e177fe62!2z0J3RjNGOLdCZ0L7RgNC6LCDQodCo0JA!5e0!3m2!1sru!2sru!4v1682574045466!5m2!1sru!2sru"
      height="100%"
      width="100%"
      style="border: 0"
      allowfullscreen=""
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
    ></iframe>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.map {
  height: 100%;
  iframe {
    filter: grayscale(100%) opacity(0.5);
  }
}
</style>
