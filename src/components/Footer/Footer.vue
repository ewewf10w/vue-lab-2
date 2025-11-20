<script setup>
import FooterAddress from './FooterAddress.vue';
import FooterContact from './FooterContact.vue';
import FooterHours from './FooterHours.vue';
import FooterCopyright from './FooterCopyright.vue';
</script>

<template>
  <footer class="site-footer">
    <div class="container">
      <div class="row">
        <FooterAddress />
        <FooterContact />
        <FooterHours />
        <FooterCopyright />
      </div>
    </div>
  </footer>
</template>
