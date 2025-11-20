<script setup>
import TestimonialsCard from './TestimonialsCard.vue';

const testimonials = [
  {
    author: {
      name: 'Sandra',
      who: 'Customers',
      avatar: '/images/reviews/young-woman-with-round-glasses-yellow-sweater.jpg',
    },
    rating: '2',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    author: {
      name: 'Don',
      who: 'Customers',
      avatar: '/images/reviews/senior-man-white-sweater-eyeglasses.jpg',
    },
    rating: '3.5',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    author: {
      name: 'Olivia',
      who: 'Customers',
      avatar:
        '/images/reviews/young-beautiful-woman-pink-warm-sweater-natural-look-smiling-portrait-isolated-long-hair.jpg',
    },
    rating: '5',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    author: {
      name: 'John',
      who: 'Customers',
      avatar: '/images/reviews/young-woman-with-round-glasses-yellow-sweater.jpg',
    },
    rating: '4.5',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
];

const generateStarsClass = (rating) => {
  const starsClass = [];
  const fullStars = Math.floor(rating); // Количество полных звезд
  const hasHalfStar = rating % 1 >= 0.5; // Нужна ли половина звезды

  for (let i = 0; i < fullStars; i++) {
    starsClass.push('bi-star-fill');
  }

  if (hasHalfStar) {
    starsClass.push('bi-star-half');
  }

  const emptyStars = 5 - fullStars - (hasHalfStar ? 1 : 0);
  for (let i = 0; i < emptyStars; i++) {
    starsClass.push('bi-star');
  }

  return starsClass;
};

defineProps({
  testimonials: Array,
});
</script>

<template>
  <section class="reviews-section section-padding section-bg" id="section_4">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-12 text-center mb-4 pb-lg-2">
          <em class="text-white">Reviews by Customers</em>
          <h2 class="text-white">Testimonials</h2>
        </div>

        <div class="timeline">
          <TestimonialsCard
            v-for="(t, i) in testimonials"
            :key="t.author.name"
            :testimonial="t"
            :index="i"
          />
        </div>
      </div>
    </div>
  </section>
</template>
