<script setup>
defineProps({
  label: String,
  id: String,
  type: { type: String, default: 'text' },
  placeholder: String,
  required: Boolean,
});
</script>

<template>
  <div class="mb-3">
    <label :for="id" class="form-label">{{ label }}</label>
    <input
      :type="type"
      :id="id"
      :placeholder="placeholder"
      class="form-control"
      :required="required"
    />
  </div>
</template>
