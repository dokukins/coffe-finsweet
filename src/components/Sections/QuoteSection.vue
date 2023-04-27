<script setup>
import { ref } from "vue";
import PlayIcon from "../Icons/PlayIcon.vue";
import YoutubeModal from "../YoutubeModal.vue";

const isModalOpen = ref(false);

const openModal = () => {
  isModalOpen.value = true;
};

const closeModal = () => {
  isModalOpen.value = false;
};
</script>

<template>
  <section class="quote">
    <div class="container-quote">
      <div class="quote__text">
        <p class="heading heading-4" :style="{ fontWeight: '500' }">
          Edit this text to make it your own. To edit, simply click directly on
          the text to start adding your own words. You can move the text by
          dragging and dropping the text
        </p>
        <div class="quote__text__author">
          <div>
            <p class="text" :style="{ color: 'white' }">Joheny Andro</p>
            <p :style="{ fontSize: '12px' }">Bhubaneswar, Odisha</p>
          </div>
          <div>
            <img src="/src/assets/avatar_image.png" alt="" />
          </div>
        </div>
        <hr />
      </div>
    </div>
    <div class="quote__video" @click="openModal">
      <img src="/src/assets/video_image.png" alt="" />
      <PlayIcon class="play-icon" />
    </div>
  </section>

  <YoutubeModal
    v-if="isModalOpen"
    class="modal__video"
    @modal-click="closeModal"
  />
</template>

<style lang="scss" scoped>
.quote {
  margin-top: 10rem;
  display: flex;
  gap: 4rem;
  background: $bg-secondary;

  .container-quote {
    display: flex;
    flex: 0 1 33%;
    justify-content: space-between;
    gap: 5rem;
  }
  &__text {
    padding: 5rem 0;

    &__author {
      margin-top: 4rem;
      display: flex;
      justify-content: space-between;
      border-bottom: 1px solid rgba(255, 255, 255, 0.24);
      & div:last-child {
        border-bottom: 2px solid white;
        padding-bottom: 1.475rem;
      }
    }
    &::before {
      content: "“";
      font-size: 4.5rem;
      line-height: 1;
      color: white;
    }
  }

  &__video {
    flex: 0 1 67%;
    position: relative;
    user-select: none;
    cursor: pointer;
    img {
      object-fit: cover;
      height: 100%;
      width: 100%;
    }
    .play-icon {
      z-index: 1;
      position: absolute;
      inset: 50%;
    }
  }
}
</style>
