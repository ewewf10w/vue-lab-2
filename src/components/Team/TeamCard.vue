<script setup>
defineProps({
  person: Object,
});
</script>

<template>
  <div class="team-block-wrap">
    <div class="team-block-info d-flex flex-column">
      <div class="d-flex mt-auto mb-3">
        <h4 class="text-white mb-0">{{ person.name }}</h4>
        <p class="badge ms-4">
          <em>{{ person.tag }}</em>
        </p>
      </div>
      <p class="text-white mb-0">{{ person.tagline }}</p>
    </div>

    <div class="team-block-image-wrap">
      <img :src="person.image" class="team-block-image img-fluid" alt="" />
    </div>
  </div>
</template>
