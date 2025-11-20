<script setup>
import TextInput from '../Forms/TextInput.vue';
import Textarea from '../Forms/TextArea.vue';
import GoogleMap from './GoogleMap.vue';
</script>

<template>
  <section class="contact-section section-padding" id="section_5">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 col-12">
          <em class="text-white">Say Hello</em>
          <h2 class="text-white mb-4 pb-lg-2">Contact</h2>
        </div>

        <div class="col-lg-6 col-12">
          <form class="custom-form contact-form" role="form">
            <div class="row">
              <div class="col-lg-6 col-12">
                <TextInput label="Name" id="name" placeholder="Jackson" required />
              </div>
              <div class="col-lg-6 col-12">
                <TextInput
                  label="Email Address"
                  id="email"
                  type="email"
                  placeholder="Jack@gmail.com"
                  required
                />
              </div>
              <div class="col-12">
                <Textarea
                  label="How can we help?"
                  id="message"
                  placeholder="Message"
                  rows="4"
                  required
                />
              </div>
            </div>
            <div class="col-lg-5 col-12 mx-auto mt-3">
              <button type="submit" class="form-control">Send Message</button>
            </div>
          </form>
        </div>

        <div class="col-lg-6 col-12 mt-5 mt-lg-0">
          <GoogleMap />
        </div>
      </div>
    </div>
  </section>
</template>
