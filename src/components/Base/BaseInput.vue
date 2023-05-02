<template>
  <input
    type="text"
    :id="id"
    :placeholder="placeholder"
    @input="$emit('update:modelValue', $event.target.value)"
  />
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
input {
  font-size: 1rem;
  border: 1px solid rgba(255, 255, 255, 0.04);
  padding: 1rem 2rem;
  color: $primary;
  background: transparent;
  &::placeholder {
    color: $primary;
  }
  &:focus {
    border: 1px solid white;
  }
}
</style>
