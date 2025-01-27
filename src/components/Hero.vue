
<template>
  <section class="relative w-full h-[50vh] md:h-[40vh] lg:h-[50vh]">
    <v-carousel hide-delimiters cycle show-arrows="hover">
      <v-carousel-item
        :src="banner1"
        cover
      ></v-carousel-item>

      <v-carousel-item
        :src="banner2"
        cover
      ></v-carousel-item>

      <v-carousel-item
        :src="banner3"
        cover
      ></v-carousel-item>
    </v-carousel>
  </section>
</template>

<script setup>
import banner1 from '@/assets/carousel_homeview/banner_home.jpg'
import banner2 from '@/assets/carousel_homeview/banner2_home.jpg'
import banner3 from '@/assets/carousel_homeview/banner3_home.jpg'
</script>

<style  scoped></style>
