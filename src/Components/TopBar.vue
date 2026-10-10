<script setup>

import { ref } from "vue";
import WhatsappButton from "../Components/Elements/WhatsappContact.vue"

const links = ref([
    { name: "Inicio", href: "#home" },
    { name: "Servicios", href: "#services" },
    { name: "Refacciones", href: "#refactions" },
    { name: "Galería", href: "#gallery" },
    { name: "Contacto", href: "#contact" },
]);

const linkClass = ref("relative text-gray-300 text-[80%] py-2 transition-colors duration-300 hover:text-blue-400 group")
</script>

<template>
<div class="top-bar sticky top-0 z-50 bg-gray-900 p-2 flex justify-between items-center shadow-md">
    <!-- Grupo Izquierda: Logo + Links -->
    <div class="flex items-center gap-6">
        <!-- Logo -->
        <div class="brand-logo min-w-[100px]">
            <img
                src="../../public/assets/images/AFA-AUT.svg"
                width="130"
                alt="Brand Logo"
            />
        </div>

        <!-- Links -->
        <div class="list-content border-1-blue-500">
            <ul class="flex items-center gap-4 text-white">
                <div v-for="link in links" :key="link.name" class="border-b-2 border-transparent hover:border-blue-400">
                    <li>
                        <a :href="link.href" :class="linkClass">
                            {{ link.name }}
                        </a>
                    </li>
                </div>
                
                <!-- <li v-for="link in links" :key="link.name">
                    <a :href="link.href" :class="linkClass">
                        {{ link.name }}
                    </a>
                </li> -->
            </ul>
        </div>
    </div>

    <WhatsappButton />

</div>
</template>

<style lang="scss">
.list-content {
    li {
        padding: 0.5rem;
    }
}
.whatsapp {
    background-color: #25D366;
}
</style>
