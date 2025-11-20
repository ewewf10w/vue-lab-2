<script setup>
defineProps({
  rating: Number,
});
</script>

<template>
  <div class="reviews-group">
    <i
      v-for="i in 5"
      :key="i"
      :class="{
        'bi-star-fill': rating >= i,
        'bi-star-half': rating >= i - 0.5 && rating < i,
        'bi-star': rating < i - 0.5,
      }"
    ></i>
  </div>
</template>
