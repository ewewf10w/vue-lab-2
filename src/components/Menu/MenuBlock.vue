<script setup>
import MenuItem from './MenuItem.vue';

defineProps({
  menu: Object,
});
</script>

<template>
  <div class="menu-block-wrap">
    <div class="text-center mb-4 pb-lg-2">
      <em class="text-white">{{ menu.name }}</em>
      <h4 class="text-white">{{ menu.type }}</h4>
    </div>

    <MenuItem v-for="i in menu.items" :key="i.name" :item="i" />
  </div>
</template>
