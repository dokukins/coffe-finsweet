<template>
  <textarea
    :name="id"
    :id="id"
    cols="30"
    rows="10"
    :placeholder="placeholder"
    @input="$emit('update:modelValue', $event.target.value)"
  ></textarea>
</template>

<script setup>
defineProps({
  modelValue: String,
  id: String,
  placeholder: String,
});

defineEmits(["update:modelValue"]);
</script>

<style lang="scss" scoped>
textarea {
  font-size: 1rem;
  border: 1px solid rgba(255, 255, 255, 0.04);
  padding: 1rem 2rem;
  color: $primary;
  background: transparent;
  &::placeholder {
    color: $primary;
  }
}
</style>
