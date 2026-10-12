<template>
  <div class=" w-full py-1 px-4 bg-gray-50">
    <div class="max-w-7xl mx-auto">

    <div class="gallery-container px-2">
        <!-- Encabezado de la galería -->
        <div class="text-center mb-2">
            <h2 class="text-2xl md:text-3xl mt-4 font-extrabold text-gray-900 tracking-wide uppercase">
                Galería
            </h2>
            <p class="text-sm md:text-base text-gray-600 mt-0">
                Algunos de nuestros trabajos y proyectos.
            </p>
        </div>

    <!-- Contenedor del Slider -->
    <div class="relative flex items-center px-4 ">
    <!-- Botón Izquierda -->
    <button
        @click="prevSlide"
        aria-label="Anterior"
        class="absolute left-0 z-10 -translate-x-2 md:-translate-x-5 bg-gray-800 hover:bg-blue-400 text-white rounded-full p-2 md:p-2.5 shadow-md transition-all duration-200 focus:outline-none flex items-center justify-center"
    >
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M15 19l-7-7 7-7" />
        </svg>
    </button>

    <!-- Carrusel / Elementos deslizables -->
    <div
        ref="slider"
        class="flex gap-4 overflow-x-auto scroll-smooth no-scrollbar py-2 mx-6 px-1 w-full"
    >
        <div
        v-for="(item, index) in images"
        :key="index"
        class="flex-none w-full sm:w-[calc(50%-8px)] md:w-[calc(33.333%-11px)] lg:w-[calc(20%-13px)] aspect-4/3 rounded-xl overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300"
        >
        <img
            :src="item.url"
            :alt="item.alt"
            class="w-full h-full object-cover rounded-xl hover:scale-105 transition-transform duration-300"
        />
        </div>
    </div>

    <!-- Botón Derecha -->
    <button
        @click="nextSlide"
        aria-label="Siguiente"
        class="absolute right-0 z-10 translate-x-2 md:translate-x-5 bg-gray-800 hover:bg-blue-400 text-white rounded-full p-2 md:p-2.5 shadow-md transition-all duration-200 focus:outline-none flex items-center justify-center"
    >
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M9 5l7 7-7 7" />
        </svg>
    </button>
    <!-- FIN Contenedor del Slider -->
    </div>


        <!-- FIN gallery-content -->
    </div >
    

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const slider = ref(null);

// Lista de imágenes

const images = ref([
    { url: '/assets/foto-1.jpg', alt: 'Proyecto 1' },
    { url: '/assets/foto-2.jpg', alt: 'Proyecto 2' },
    { url: '/assets/foto-3.jpg', alt: 'Proyecto 3' },
    { url: '/assets/foto-4.jpg', alt: 'Proyecto 4' },
    { url: '/assets/foto-5.jpg', alt: 'Proyecto 5' },
    { url: '/assets/foto-6.jpg', alt: 'Proyecto 6' },
    { url: '/assets/foto-7.jpg', alt: 'Proyecto 7' },
    { url: '/assets/foto-8.jpg', alt: 'Proyecto 8' },
    { url: '/assets/foto-9.jpg', alt: 'Proyecto 9' },
    { url: '/assets/foto-10.jpg', alt: 'Proyecto 10' },
    { url: '/assets/foto-11.jpg', alt: 'Proyecto 11' },
]);

// Funciones para desplazar el slider
const nextSlide = () => {
    if (slider.value) {
    slider.value.scrollLeft += slider.value.clientWidth;
    }
};

const prevSlide = () => {
    if (slider.value) {
    slider.value.scrollLeft -= slider.value.clientWidth;
    }
};
</script>

<style scoped>
/* Ocultar barra de desplazamiento manteniendo la funcionalidad */
.no-scrollbar::-webkit-scrollbar {
    display: none;
}
.no-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.gallery-container {

}
</style>