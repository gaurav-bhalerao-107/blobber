<template>
  <section class="index-page tw-relative">
    <main class="tw-relative tw-bg-white hero-wrapper tw-w-full">
      <div class="tw-w-full">
        <div class="moving-blob tw-fixed tw-inset-0 tw-mx-auto tw-mt-5"></div>
      </div>
      <main class="tw-relative tw-z-10">
        <div class="tw-pt-28">
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
                <h1 class="tw-text-4xl tw-font-bold tw-tracking-tight tw-text-center sm:tw-text-6xl">Blob Generator to enrich your website</h1>
              </div>
            </div>
          </div>
        </div>
      </main>

      <main class="tw-relative tw-flex tw-items-center tw-justify-center tw-w-full">
        <div class="max-width-handler tw-px-3 sm:tw-px-5 lg:tw-px-10 tw-w-full">
          <div class="tw-flex tw-flex-col tw-py-10 lg:tw-flex-row tw-justify-between tw-w-full">
            <div class="tw-relative tw-mb-5 tw-z-10">
              <div class="card_background tw-shadow-lg tw-py-10 tw-px-0 md:tw-px-12 tw-h-full tw-w-full  tw-flex tw-items-center tw-justify-center">
                <div class="blob" :style="{'border-radius': blob_parameters.radius_1 + '%' + blob_parameters.radius_2 + '%' + blob_parameters.radius_3 + '%' + blob_parameters.radius_4 + '%' + '/' + blob_parameters.radius_5 + '%' + blob_parameters.radius_6 + '%' + blob_parameters.radius_7 + '%' + blob_parameters.radius_8 + '%'}"></div>
                <div  class="tw-absolute tw-mx-auto tw-mt-12" style="cursor: pointer; bottom: -30px"> 
                  <!-- random -->
                  <q-icon @click="randomBlobGenerator()" name="refresh" class="text-white tw-bg-indigo-600 tw-p-5 tw-rounded-xl" style="font-size: 2em;" /> 
                  
                  <!-- download -->
                  <q-icon @click="domToImage()" name="download" class="text-white tw-bg-indigo-600 tw-p-5 tw-rounded-xl tw-mx-2" style="font-size: 2em;" /> 
                  
                  <!-- color -->
                  <!-- <q-icon  name="color" class="tw-text-red-700 tw-bg-red-700 tw-p-5 tw-rounded-xl" style="font-size: 2em;"> 
                    <q-popup-proxy transition-show="scale" transition-hide="scale">
                      <q-color v-model="blob_color" />
                    </q-popup-proxy>
                  </q-icon>  -->
                </div>
              </div>
            </div>

            <div class="tw-flex-1 lg:tw-pl-5 tw-grid tw-grid-cols-1 tw-gap-8 md:tw-grid-cols-2 tw-mt-7 lg:tw-mt-0">
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10 tw-mb-5">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 1</label>
                <q-slider
                  v-model="blob_parameters.radius_1" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10 tw-mb-5">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 2</label>
                <q-slider
                  v-model="blob_parameters.radius_2" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 3</label>
                <q-slider
                  v-model="blob_parameters.radius_3" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 4</label>
                <q-slider
                  v-model="blob_parameters.radius_4" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10 tw-mb-5">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 5</label>
                <q-slider
                  v-model="blob_parameters.radius_5" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10 tw-mb-5">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 6</label>
                <q-slider
                  v-model="blob_parameters.radius_6" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10 tw-mb-5">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 7</label>
                <q-slider
                  v-model="blob_parameters.radius_7" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
              <div class="tw-w-full tw-px-5 tw-pb-7 tw-pt-3 tw-shadow-lg card_background tw-z-10 tw-mb-5">
                <label class="tw-text-black tw-font-semibold tw-text-xl">Radius 8</label>
                <q-slider
                  v-model="blob_parameters.radius_8" 
                  :min="0" 
                  :max="100"
                  color="deep-orange"
                  label
                  label-always
                  switch-label-side
                  track-size="8px"
                  inner-track-color="transparent"
                />
              </div>
            </div>
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
import _ from 'lodash';

export default defineComponent({
  name: "IndexPage",

  components:{
    CardVue
  },

  data() {
    return {
      blob_parameters: {
        height: 0,
        width: 0,
        radius_1: 70,
        radius_2: 30,
        radius_3: 30,
        radius_4: 70,
        radius_5: 60,
        radius_6: 40,
        radius_7: 60,
        radius_8: 40,
      },
      blob_color: '#FF00FFCC'
    };
  },

  methods: {
    domToImage(){
      let self = this;

      self.$q.loading.show();
      let node = document.getElementsByClassName('blob')[0]
      domtoimage.toPng(node)
      .then((dataUrl) => {
          var img = new Image();
          img.src = dataUrl;

          self.$q.loading.hide();

          const downloadLink = document.createElement("a");
          downloadLink.href = dataUrl;
          downloadLink.download = 'blobber.png';
          downloadLink.click();
      })
      .catch((error) => {
        console.error('oops, something went wrong!', error);
        self.$q.loading.hide();
      });
    },

    randomBlobGenerator(){
      this.blob_parameters.radius_1 = _.random(10, 100)
      this.blob_parameters.radius_2 = _.random(10, 100)
      this.blob_parameters.radius_3 = _.random(10, 100)
      this.blob_parameters.radius_4 = _.random(10, 100)
      this.blob_parameters.radius_5 = _.random(10, 100)
      this.blob_parameters.radius_6 = _.random(10, 100)
      this.blob_parameters.radius_7 = _.random(10, 100)
      this.blob_parameters.radius_8 = _.random(10, 100)
    }
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

  .blob {
    width: 360px;
    height: 360px;
    background-color: #7f00ff;
    background: linear-gradient(to right, #7f00ff, #e100ff);
    box-shadow: 0 0 10px rgba(0, 0, 0, .3);
    z-index: 2;
  }

  .moving-blob{
    width: 500px;
    height: 500px;
    background: linear-gradient(180deg, rgba(47, 184, 255,0.42) 31.77%, #5c9df1 100%);
    -webkit-animation: move 25s infinite alternate; 
    animation: move 10s infinite alternate;
    transition: 1s cubic-bezier(0.1, 0.7, 1.0, 0.1);
  }

  @media only screen and (max-width: 720px)  {
    .moving-blob{
      width: 300px;
      height: 300px;
      background: linear-gradient(
        180deg,
        rgba(47, 184, 255,0.42) 31.77%,
        #5c9df1 100%
      );
      -webkit-animation: move 25s infinite alternate; 
      animation: move 10s infinite alternate;
      transition: 1s cubic-bezier(0.1, 0.7, 1.0, 0.1);
    }
  }

  .card {
    width: 400px;
    min-height: 250px;
    background: rgba( 255, 255, 255, 0.15 );
    box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
    backdrop-filter: blur( 18px );
    -webkit-backdrop-filter: blur( 18px );
    border: 1px solid rgba( 255, 255, 255, 0.18 );
    border-radius: 1rem;
    padding: 1.5rem;
    z-index: 10;
    color: whitesmoke;
  }

  @-webkit-keyframes move {
    from {
      /* transform: translate(10px, 10px) rotate(-90deg); */
      border-radius: 24% 76% 35% 65% / 27% 36% 64% 73%;
    }

    to {
      /* transform: translate(100%, 10px) rotate(-10deg); */
      border-radius: 76% 24% 33% 67% / 68% 55% 45% 32%;
    }
  }

  @keyframes move {
    from {
      /* transform: translate(10px, 10px) rotate(-10deg); */
      border-radius: 24% 76% 35% 65% / 27% 36% 64% 73%;
    }

    to {
      /* transform: translate(100%, 10px) rotate(-90deg); */
      border-radius: 76% 24% 33% 67% / 68% 55% 45% 32%;
    }
  }

  .card_background{
    background: rgba( 255, 255, 255, 0.15 );
    box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
    backdrop-filter: blur( 18px );
    -webkit-backdrop-filter: blur( 18px );
    border: 1px solid rgba( 255, 255, 255, 0.18 );
    border-radius: 1rem;
    color: whitesmoke;
  }
</style>
