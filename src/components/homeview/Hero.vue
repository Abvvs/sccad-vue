<template>
  <section class="relative w-full h-[50vh] md:h-[40vh] lg:h-[50vh]">
    <!-- Texto y botón superpuestos -->
    <div
      class="absolute top-0 left-0 w-full h-full flex flex-col items-center justify-center bg-black/50 text-white text-center px-4 z-10">
      <h1 class="text-4xl font-bold mb-2">SCCAD</h1>
      <p class="text-lg mb-4">La mejor solución para tus necesidades. Conócenos mejor y descubre lo que podemos
        ofrecerte.</p>
      <v-btn variant="tonal">Contáctanos</v-btn>
    </div>

    <!-- Carrusel -->
    <v-carousel hide-delimiters cycle :show-arrows="false" class="z-0" height="100%">
      <v-carousel-item :src="banner1" cover></v-carousel-item>

      <v-carousel-item :src="banner2" cover></v-carousel-item>

      <v-carousel-item :src="banner3" cover></v-carousel-item>
    </v-carousel>
  </section>
</template>

<script setup>
import banner1 from '@/assets/carousel_homeview/banner_home.jpg'
import banner2 from '@/assets/carousel_homeview/banner2_home.jpg'
import banner3 from '@/assets/carousel_homeview/banner3_home.jpg'
</script>

<style scoped></style>
