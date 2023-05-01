<script setup>
import { computed } from "vue";

const props = defineProps({
  label: String,
  id: String,
  value: {
    type: String,
    default: "",
  },
  modelValue: {
    type: String,
    default: "",
  },
});

const emits = defineEmits(["update:modelValue"]);

const isChecked = computed(() => {
  return props.modelValue == props.value;
});
</script>

<template>
  <label :class="['menu__filter', { active: isChecked }]" :for="id">
    <input
      type="radio"
      name="filter"
      :id="id"
      :value="value"
      :checked="isChecked"
      @change="$emit('update:modelValue', $event.target.value)"
    />
    {{ label }}
  </label>
</template>

<style lang="scss" scoped>
.menu__filter {
  cursor: pointer;
  transition: color 0.2s;
  input {
    display: none;
  }
  &:hover {
    color: rgba($color: $secondary, $alpha: 0.7);
  }
}

.active {
  color: $primary;
  border-bottom: 4px solid $primary;
}
</style>
