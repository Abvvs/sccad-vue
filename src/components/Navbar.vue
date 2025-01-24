<script setup>
import { RouterLink } from "vue-router";
import IconXMark from "../components/icons/IconXMark.vue";
import IconMenu from "../components/icons/IconMenu.vue";
import { ref } from "vue";

const open = ref(false);
const toggleMenu = () => {
  open.value = !open.value;
};
</script>

<template>
  <header
    class="flex justify-between items-center bg-white shadow-md h-[80px] px-5 lg:px-24 relative z-10"
  >
    <div
      class="text-3xl font-extrabold text-red-700 hover:text-red-800 cursor-pointer"
    >
      <RouterLink to="/">SCCAD</RouterLink>
    </div>
    <nav
      class="flex flex-col md:flex-row p-5 gap-4 md:gap-10 px-6 md:static absolute bg-white md:bg-transparent shadow-md md:shadow-none md:w-auto my-7 md:my-0 left-0 w-full duration-500" :class="[open ? 'top-0': 'top-[-390%]']"
    >
      <!-- hacer reutilizable esta parte de los links del nav -->
      <RouterLink
        class="text-red-500 p-5 hover:text-red-700 text-xl font-medium"
        to="/"
      >
        Inicio
      </RouterLink>
      <RouterLink
        class="text-red-500 p-5 hover:text-red-700 text-xl font-medium"
        to="/about"
      >
        Sobre Nosotros
      </RouterLink>
      <RouterLink
        class="text-red-500 p-5 hover:text-red-700 text-xl font-medium"
        to="/"
      >
        Consulta de trámites
      </RouterLink>
    </nav>
    <div class="text-4xl text-black cursor-pointer md:hidden z-20" @click="toggleMenu">
      <component :is="open ? IconXMark : IconMenu" />
    </div>
  </header>
</template>
