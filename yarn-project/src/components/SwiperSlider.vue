<template>
  <div class="carousel-wrapper">
     <q-carousel
       v-model="slide"
       transition-prev="slide"
       transition-next="slide"
       swipeable
       animated
       control-color="primary"
       navigation-icon="radio_button_unchecked"
       navigation
     >
       <q-carousel-slide name="first" img-src="https://hcdn.kartalyuvasi.com.tr/mnresize/1920/-/kartalyuvasi/UPLOAD/banner/anasayfa-slider/Desktop/yilsonu_indirim_banner_tr.jpg">
         <div class="custom-bottom">
           <div class="text-h2">First stop</div>
           <div class="text-subtitle1">Yannic Murat</div>
         </div>
       </q-carousel-slide>
       <q-carousel-slide
         name="second"
         img-src="https://hcdn.kartalyuvasi.com.tr/kartalyuvasi/UPLOAD/banner/koleksiyon/adidas-champion-collection-1024.jpg"
       >
         <div class="custom-bottom">
           <div class="text-h2">Second stop</div>
           <div class="text-subtitle1">Adidas Champion Collection</div>
         </div>
       </q-carousel-slide>
       <q-carousel-slide
         name="third"
         img-src="https://hcdn.kartalyuvasi.com.tr/kartalyuvasi/UPLOAD/banner/koleksiyon/KRTLYVS_SonbaharKoleksiyon_Banner.jpg"
       >
         <div class="custom-bottom">
           <div class="text-h2">Third stop</div>
           <div class="text-subtitle1">KRTLYVS Sonbahar Koleksiyon</div>
         </div>
       </q-carousel-slide>
     </q-carousel>
  </div>
 </template>
 
 <script lang="ts">
 import { defineComponent, ref } from 'vue';
 
 export default defineComponent({
  setup() {
     return {
       slide: ref('first'),
     };
  },
 });
 </script>
 <style scoped>
 /* Add your custom styles here */
 .custom-bottom {
 position: absolute;
 bottom: 20px;
 left: 20px;
 right: 20px;
}
 </style>
 