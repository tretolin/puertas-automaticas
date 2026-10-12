<script setup>
import TopBar from "./Components/TopBar.vue";
import HeroImage from "./Components/HeroImage.vue";
import Servicios from "./Components/Servicios.vue";
import Refacciones from "./Components/Refacciones.vue";
import Gallery from "./Components/Gallery.vue";
import Contacto from "./Components/Contacto.vue";
import Footer from "./Components/Footer.vue";
</script>
<template>
    <div
        class="main-content pt-2 p-2 bg-gray-900 text-white w-full"
    >
        <!-- TopBar -->
        <TopBar id="top-bar" />

        <!-- Hero Image -->
        <section>
            <HeroImage id="home" class=" mt-15" />
        </section>

        <!-- Servicios -->
        <section id="services" class="scroll-mt-20">
            <Servicios />
        </section>

        <!-- Refacciones -->
        <section id="refactions" class="scroll-mt-20">
            <Refacciones />
        </section>

        <!-- Galería -->
        <section id="gallery" class="scroll-mt-20">
            <Gallery />
        </section>

        <!-- Contacto -->
        <section id="contact" class="scroll-mt-20">
            <Contacto />
        </section>

        <!-- Footer -->
        <section>
            <Footer />
        </section>
    </div>
</template>
<style lang="scss">
</style>
