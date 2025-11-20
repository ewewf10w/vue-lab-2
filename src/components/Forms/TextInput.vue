<script setup>
const model = defineModel();
defineProps({
  label: String,
  id: String,
  type: { type: String, default: 'text' },
  required: Boolean,
});
</script>

<template>
  <label :for="id" class="form-label">{{ label }}</label>
  <input :id="id" :type="type" v-model="model" class="form-control" :required="required" />
</template>
