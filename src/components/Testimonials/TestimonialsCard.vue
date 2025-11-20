<script setup>
import rating from '../Testimonials/Rating.vue';

defineProps({
  testimonial: Object,
  index: Number,
});
</script>

<template>
  <div :class="{ 'timeline-container-right': index % 2 === 1 }" class="timeline-container">
    <div class="timeline-content">
      <div class="reviews-block">
        <div class="reviews-block-image-wrap d-flex align-items-center">
          <img :src="testimonial.author.avatar" class="reviews-block-image img-fluid" alt="" />
          <div>
            <h6 class="text-white mb-0">{{ testimonial.author.name }}</h6>
            <em class="text-white">{{ testimonial.author.who }}</em>
          </div>
        </div>

        <div class="reviews-block-info">
          <p>{{ testimonial.descr }}</p>

          <div class="d-flex border-top pt-3 mt-4">
            <strong class="text-white">{{ testimonial.rating }}</strong>
            <Rating :rating="Number(testimonial.rating)" class="ms-auto" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
