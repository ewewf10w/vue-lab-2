<script setup>
import FooterBrand from './FooterBrand.vue';
import OpeningHours from './OpeningHours.vue';
import FooterContact from './FooterContact.vue';
import SocialLinks from './SocialLinks.vue';
</script>

<template>
  <footer class="site-footer section-padding" id="section_6">
    <div class="container">
      <div class="row">
        <div class="col-lg-4 col-md-6 col-12 mb-3">
          <FooterBrand />
        </div>

        <div class="col-lg-4 col-md-6 col-12 mb-3">
          <OpeningHours />
        </div>

        <div class="col-lg-4 col-md-12 col-12">
          <FooterContact />
          <SocialLinks />
        </div>
      </div>

      <div class="row mt-4">
        <div class="col-12 text-center">
          <p class="text-white mb-0">© 2025 Barista.co — All Rights Reserved.</p>
        </div>
      </div>
    </div>
  </footer>
</template>
