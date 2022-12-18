<template>
  <section class="index-page">
    <main class="tw-relative tw-pt-32 hero-wrapper">
      <section class="pattern tw-h-96">
      </section>
    </main>
  </section>
</template>

<script>
import { defineComponent } from "vue";
import domtoimage from 'dom-to-image';
import _ from 'lodash';

export default defineComponent({
  name: "Waves",

  data() {
    return {
      
    };
  },

  methods: {
    
  },

  mounted() {
    
  },
});
</script>


<style>
.pattern {
  position: relative;
  background-color: #21D4FD;
  background-image: linear-gradient(19deg, #21D4FD 0%, #B721FF 100%);
}
</style>