<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="tw-isolate" :class="changeNavColor ? 'tw-bg-white' : 'tw-bg-transparent'">
      <header>
        <div class="tw-relative tw-z-10 tw-px-6 tw-py-4 lg:tw-px-8">
          <div class="tw-flex tw-w-full tw-items-center tw-justify-center">
            <a href="">
              <span class="tw-font-bold tw-text-indigo-600 text-center tw-text-3xl sm:tw-text-5xl">Blobber</span>
            </a>
          </div>
        </div>
      </header>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'


export default defineComponent({
  name: 'MainLayout',

  data(){
    return {
      changeNavColor: false
    }
  },

  computed: {
    
  },

  methods: {
    handleScroll() {
      let position = window.pageYOffset;
      if (position >= 50){
        this.changeNavColor = true
      }else{
        this.changeNavColor = false
      }
    },
  },

  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  },

  mounted(){
    window.addEventListener('scroll', this.handleScroll, { passive: true });
  }
})
</script>

<style>

</style>