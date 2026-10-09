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
  <div class="main-content p-2 border-1-gray-300 bg-gray-900 text-white">
    <!-- <TopBar/> ----------------->
    <section>
      <div><TopBar /></div>
    </section>

    <!-- <Hero Image/> ----------------->
    <section>
      <div><HeroImage /></div>
    </section>

    <!-- <Servicios/> ----------------->
    <section>
      <div><Servicios /></div>
    </section>

    <!-- <Refacciones/> ----------------->
    <section>
      <div><Refacciones /></div>
    </section>

    <!-- <Galería/> ----------------->
    <section>
      <div><Gallery /></div>
    </section>

    <!-- <Contacto/> ----------------->
    <section>
      <div><Contacto /></div>
    </section>

    <!-- <Footer/> ----------------->
    <section>
      <div><Footer /></div>
    </section>
  </div>
</template>
<style lang="scss">
</style>
