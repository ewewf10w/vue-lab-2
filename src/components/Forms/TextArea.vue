<script setup>
const model = defineModel();
defineProps({
  label: String,
  id: String,
  rows: { type: Number, default: 4 },
  placeholder: String,
  required: Boolean,
});
</script>

<template>
  <div class="mb-3">
    <label :for="id" class="form-label">{{ label }}</label>
    <textarea
      :id="id"
      :rows="rows"
      :placeholder="placeholder"
      class="form-control"
      :required="required"
      v-model="model"
    ></textarea>
  </div>
</template>
