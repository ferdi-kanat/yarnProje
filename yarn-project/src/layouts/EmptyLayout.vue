<template>
  <q-layout view="lHh Lpr lFf">
    <!-- ... Diğer layout kodları ... -->

    <q-page-container>
      <!-- <router-view /> yerine doğrudan TheSlide1 componentini ekleyin -->
      <TheSlide1 />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import TheSlide1 from 'src/components/TheSlide1.vue';
// Gerekli setup kodları buraya
</script>
