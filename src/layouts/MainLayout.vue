<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="tw-isolate tw-bg-white">
      <header>
        <div class="tw-px-6 tw-py-4 lg:tw-px-8">
          <div class="tw-flex tw-w-full tw-items-center tw-justify-center">
            <a href="">
              <span class="tw-font-bold tw-text-indigo-600 text-center tw-text-5xl">Blobber</span>
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

    }
  },

  computed: {
    
  },

  methods: {
    
  },

  mounted(){
    
  }
})
</script>

<style>

</style>