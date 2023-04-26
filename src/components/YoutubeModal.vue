<template>
  <div class="modal">
    <div class="modal__content">
      <div class="modal__header"></div>
      <div class="modal__body">
        <iframe
          width="1000"
          height="500"
          src="https://www.youtube.com/embed/GuDJScFuJCk"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          allowfullscreen
        ></iframe>
      </div>
      <div class="modal__footer">
        <button @click="$emit('modalClick')">X</button>
      </div>
    </div>
  </div>
</template>

<script setup>
defineEmits(["modalClick"]);
</script>

<style lang="scss" scoped>
.modal {
  z-index: 2;
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  overflow: auto;
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.4);

  &__content {
    position: relative;
  }

  &__body {
    width: 100%;
    height: 100%;
  }

  &__footer {
    display: flex;
    justify-content: center;
    margin-top: 1rem;
    button {
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      border-radius: 50%;
      width: 4rem;
      height: 4rem;
      background: white;
      padding: 1rem;
    }
  }
}
</style>
