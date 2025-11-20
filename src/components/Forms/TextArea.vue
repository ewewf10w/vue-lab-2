<script setup>
const model = defineModel();
defineProps({
  label: String,
  id: String,
  rows: { type: Number, default: 4 },
  required: Boolean,
});
</script>

<template>
  <label :for="id" class="form-label">{{ label }}</label>
  <textarea
    v-model="model"
    :id="id"
    :rows="rows"
    class="form-control"
    :required="required"
  ></textarea>
</template>
