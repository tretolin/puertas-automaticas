<script setup>
import { ref } from "vue";
import WhatsappButton from "../Components/Elements/WhatsappContact.vue";

const links = ref([
    { name: "Inicio", href: "#home" },
    { name: "Servicios", href: "#services" },
    { name: "Refacciones", href: "#refactions" },
    { name: "Galería", href: "#gallery" },
    { name: "Contacto", href: "#contact" },
]);

const linkClass = ref("relative text-gray-300 text-[80%] py-2 transition-colors duration-300 hover:text-blue-400 group");

// Estado para controlar si el menú móvil está abierto o cerrado
const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
    isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const closeMobileMenu = () => {
    isMobileMenuOpen.value = false;
};
</script>

<template>
<!-- Cambiamos sticky por fixed w-full y z-50 (asegúrate de no usar z-1000 ya que Tailwind usa escala estándar como z-50 o z-[1000]) -->
<nav class="bg-gray-900 fixed top-0 left-0 w-full z-50 border-b border-gray-800 shadow-md">
    <div class="max-w-screen-xl px-4 py-2 flex justify-between items-center mx-auto">
        
        <!-- Logo -->
        <div class="brand-logo min-w-[100px]">
            <img
                src="../../public/assets/images/AFA-AUT.svg"
                width="130"
                alt="Brand Logo"
            />
        </div>

        <!-- Links (Escritorio) -->
        <div class="hidden md:flex list-content">
            <ul class="flex items-center gap-6 text-white">
                <li v-for="link in links" :key="link.name" class="border-b-2 border-transparent hover:border-blue-400">
                    <a :href="link.href" :class="linkClass">
                        {{ link.name }}
                    </a>
                </li>
            </ul>
        </div>

        <!-- Botón de WhatsApp (Escritorio) -->
        <div class="hidden md:block">
            <WhatsappButton />
        </div>

        <!-- Botón Hamburguesa (Móvil) -->
        <button 
            @click="toggleMobileMenu" 
            class="md:hidden text-gray-300 hover:text-blue-400 focus:outline-none p-2"
            aria-label="Abrir menú"
        >
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path v-if="!isMobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
        </button>
    </div>

    <!-- Menú Desplegable Móvil (Aparece debajo de la barra fija en cualquier posición de scroll) -->
    <div v-if="isMobileMenuOpen" class="md:hidden bg-gray-900 border-t border-gray-800 px-4 pt-2 pb-4 shadow-lg">
        <ul class="flex flex-col gap-3 text-white">
            <li v-for="link in links" :key="link.name" class="border-b border-gray-800 pb-2">
                <a 
                    :href="link.href" 
                    :class="linkClass" 
                    @click="closeMobileMenu"
                    class="block w-full"
                >
                    {{ link.name }}
                </a>
            </li>
            <!-- Botón de WhatsApp también disponible en el menú móvil si se desea -->
            <div class="pt-2">
                <WhatsappButton />
            </div>
        </ul>
    </div>
</nav>
</template>