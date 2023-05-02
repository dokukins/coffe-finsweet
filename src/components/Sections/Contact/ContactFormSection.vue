<script setup>
import BaseButton from "../../Base/BaseButton.vue";
import BaseInput from "../../Base/BaseInput.vue";
import BaseTextArea from "../../Base/BaseTextArea.vue";
import ArrowIcon from "../../Icons/ArrowIcon.vue";
import { ref } from "vue";

const images = ["contact_form_image_1.png", "contact_form_image_2.png"];

const emailValue = ref("");
const nameValue = ref("");
const messageValue = ref("");

const sendForm = () => {
  console.log({
    email: emailValue.value,
    name: nameValue.value,
    messageValue: messageValue.value,
  });
};
</script>

<template>
  <section class="contact-form">
    <div class="container flex">
      <div class="contact-form__text">
        <div class="contact-form__text__main">
          <h1 class="heading heading-1">
            Have a Question ? Get in Touch with us 👋
          </h1>
          <p class="text">
            Fill up the Form and ou team will get back to within 24 hrs
          </p>
        </div>

        <form @submit.prevent>
          <div>
            <BaseInput v-model="nameValue" placeholder="Name" id="name" />
            <BaseInput v-model="emailValue" placeholder="Email" id="email" />
          </div>
          <BaseTextArea
            v-model="messageValue"
            placeholder="Message"
            id="message"
          />
          <button type="submit" class="form-btn" @click="sendForm">
            Send Messege
            <ArrowIcon color="#FFC492" />
          </button>
        </form>
      </div>

      <div class="contact-form__img">
        <img
          v-for="img in images"
          :key="img"
          :src="`/src/assets/${img}`"
          alt=""
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.form-btn {
  padding: 1.25rem 2rem;
  color: $primary;
  font-size: 1rem;
  background: #27252d;
  max-width: 200px;
}
.flex {
  gap: 6rem;
}
.contact-form {
  margin: 10rem 0;

  form {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    div {
      display: flex;
      justify-content: space-between;
    }
  }

  &__text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2.5rem;
    padding-bottom: 5rem;
  }

  &__img {
    min-width: fit-content;
    display: flex;
    gap: 4rem;
    img {
      object-fit: contain;
      &:first-child {
        align-self: flex-end;
      }
      &:last-child {
        align-self: flex-start;
      }
    }
  }
}
</style>
