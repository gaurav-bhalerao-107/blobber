<template>
  <section class="index-page">
    <main class="tw-relative tw-max-w-7xl tw-mx-auto tw-bg-white hero-wrapper">
      <main class="">
        <div class="tw-py-32">
          <div class="tw-mx-auto tw-max-w-3xl tw-px-3">
            <div>
              <div class="tw-mb-8 tw-flex sm:tw-justify-center">
                <div class="tw-relative tw-overflow-hidden tw-rounded-full tw-py-1.5 tw-px-4 tw-text-sm tw-leading-6 tw-ring-1 ring-gray-900/10 hover:ring-gray-900/20">
                  <span class="tw-text-gray-600">
                    More interesting generators yet to come <a href="#" class="tw-font-semibold tw-text-indigo-600"><span class="tw-absolute tw-inset-0" aria-hidden="true"></span>Read more <span aria-hidden="true">&rarr;</span></a>
                  </span>
                </div>
              </div>
              <div>
                <h1 class="tw-text-4xl tw-font-bold tw-tracking-tight tw-text-center sm:tw-text-6xl">Generators to enrich your website</h1>
                <p class="tw-mt-6 tw-text-lg tw-leading-8 tw-text-gray-600 tw-text-center">Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo. Elit sunt amet fugiat veniam occaecat fugiat aliqua.</p>
                <div class="tw-mt-8 tw-flex tw-gap-x-4 tw-justify-center">
                  <a href="#" class="tw-inline-block tw-rounded-lg tw-bg-indigo-600 tw-px-4 tw-py-1.5 tw-text-base tw-font-semibold tw-leading-7 tw-text-white tw-shadow-sm tw-ring-1 tw-ring-indigo-600 hover:tw-bg-indigo-700 hover:tw-ring-indigo-700">
                    Get started
                    <span class="tw-text-indigo-200" aria-hidden="true">&rarr;</span>
                  </a>
                  <a href="#" class="tw-inline-block tw-rounded-lg tw-px-4 tw-py-1.5 tw-text-base tw-font-semibold tw-leading-7 tw-text-gray-900 tw-ring-1 ring-gray-900/10 hover:ring-gray-900/20">
                    Live demo
                    <span class="tw-text-gray-400" aria-hidden="true">&rarr;</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>

      <main class="tw-pb-10">
        <div class="tw-grid tw-grid-cols-1 tw-gap-8 sm:tw-grid-cols-2 lg:tw-grid-cols-3">
          <router-link to="/blob" data-aos="fade-up" class="tw-flex tw-flex-col">
            <CardVue class="" image="~assets/index-page-potrait.jpg" head_tag="BLOB" title="Blob Generator" description="" />
          </router-link>
          <div data-aos="fade-up" class="tw-flex tw-flex-col">
            <CardVue class="" image="~assets/index-page-potrait.jpg" head_tag="WAVES" title="Waves Generator" description="Appointment generation services is a crucial step in building a strong sales structure in an organization. It focuses on evolving your business with your prospective leads and is often referred to as a clear cut solution" />
          </div>
          <div data-aos="fade-up" class="tw-flex tw-flex-col">
            <CardVue class="" image="~assets/index-page-potrait.jpg" head_tag="SERVICES" title="Email Marketing" description="Email marketing is sending commercial emails to a list of contacts who have given their express permission to receive email communications from you" />
          </div>
        </div>
      </main>

      
    </main>
  </section>
</template>

<script>
import CardVue from "src/components/Card.vue";
import { defineComponent } from "vue";
import domtoimage from 'dom-to-image';

export default defineComponent({
  name: "IndexPage",

  components:{
    CardVue
  },

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
  .blur-effect {
    filter        : blur(10px);
    -moz-filter   : blur(10px);
    -webkit-filter: blur(10px);
    -o-filter     : blur(10px);

    transition        : all 2s linear;
    -moz-transition   : all 2s linear;
    -webkit-transition: all 2s linear;
    -o-transition     : all 2s linear;
  }
</style>
