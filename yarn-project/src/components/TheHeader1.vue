<template>
  <q-header class="bg-primary text-black">
     <q-toolbar>
       <q-toolbar-title>{{ title }}</q-toolbar-title>
       <div class="header-right">
         <q-btn
           class="r-menu"
           flat
           no-caps
           rounded
           :ripple="false"
         >
           <q-icon class="icon-globe" name="language" />
           <span>ENGLISH/€</span>
         </q-btn>
 
         <q-btn
           class="r-menu"
           to="/satis-noktalarimiz"
           unelevated
           no-caps
           rounded
           :ripple="false"
         >
          
           <span>SATIŞ NOKTALARI</span>
         </q-btn>
 
         <q-btn
           class="r-menu"
           to="/siparis-takip"
           unelevated
           no-caps
           rounded
           :ripple="false"
         >
           <span>SİPARİŞ TAKİP</span>
         </q-btn>
 
         <q-btn
           class="r-menu"
           to="/hediyekarti"
           unelevated
           no-caps
           rounded
           :ripple="false"
         >
           <q-icon class="icon-gift-card2" name="card_giftcard" />
           <span>GIFT CARD</span>
         </q-btn>
 
         <q-btn
           class="r-menu"
           to="/hesabim"
           unelevated
           no-caps
           rounded
           :ripple="false"
         >
           <q-icon class="icon-user" name="person" />
           <span>HESABIM</span>
         </q-btn>
 
         <q-btn
           class="r-menu"
           to="/sepetim"
           unelevated
           no-caps
           rounded
           :ripple="false"
         >
           <q-icon class="icon-cart" name="shopping_cart" />
           <span>ÜRÜN</span>
         </q-btn>
       </div>
     </q-toolbar>
  </q-header>
 </template>
 
 <script lang="ts">
 import { defineComponent, ref } from 'vue';
 
 export default defineComponent({
  name: 'TheHeader',
  setup() {
     const title = ref('Besiktas JK Official Shopping Site');
 
     return { title };
  },
 });
 </script>
 
 <style scoped>
 .header-right {
 display: flex;
 align-items: center;
 justify-content: flex-end;
 background-color: rgb(255, 255, 255);
 box-sizing: border-box;
 color: rgb(0, 0, 0);
 font-family: DINPro, arial, sans-serif;
 font-size: 15px;
 height: 70px;
 line-height: 19.5px;
 position: absolute;
 right: -6px;
 text-align: left;
 top: 0px;
 width: 272px;
 z-index: 0;
 }

 .r-menu {
 margin-left: 10px;
 }

 .r-menu-item {
 display: flex;
 align-items: center;
 margin-right: 20px;
 }

 .icon-globe {
 font-size: 24px;
 margin-right: 4px;
 }



 .icon-user {
 font-size: 24px;
 margin-right: 4px;
 }

 .icon-cart {
 font-size: 24px;
 margin-right: 4px;
 }

 .icon-gift-card2 {
 font-size: 24px;
 margin-right: 4px;
 }
</style>