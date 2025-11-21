<script setup>
const model = defineModel();
defineProps({
  label: String,
  id: String,
  type: { type: String, default: 'text' },
  placeholder: String,
  required: { type: Boolean, default: false },
});
</script>

<template>
  <div class="mb-3">
    <label :for="id" class="form-label">
      {{ label }}
      <sup v-if="required" class="text-danger">*</sup>
    </label>
    <input
      :type="type"
      :id="id"
      :placeholder="placeholder"
      class="form-control"
      :required="required"
      v-model="model"
    />
  </div>
</template>
