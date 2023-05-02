<script setup>
import ContactMap from "./ContactMap.vue";
</script>

<template>
  <section class="contact">
    <div class="container flex">
      <div class="contact__text">
        <div>
          <h4 class="heading heading-2">Working Hour</h4>
          <p class="text">Sunday to Saturday 09:00 AM to 11:00 PM</p>
        </div>
        <div>
          <h4 class="heading heading-2">Location</h4>
          <p class="text">Street - 127, New York,United States 546544</p>
        </div>
        <div>
          <h4 class="heading heading-2">Contact us</h4>
          <p class="text">+123456789 hey@yourdomain.com</p>
        </div>
      </div>
      <div class="contact__map">
        <ContactMap />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.contact {
  margin-top: 10rem;
  margin-bottom: 10rem;

  &__text {
    background: $bg-secondary;
    padding: 5rem 4rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
    div {
      width: 70%;
    }
  }

  &__map {
    width: 100%;
  }
}
</style>
