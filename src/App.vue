<script setup>

import TopBar from './Components/TopBar.vue'
import HeroImage from './Components/HeroImage.vue'
import Servicios from './Components/Servicios.vue'
import Refacciones from './Components/Refacciones.vue'
import Contacto from './Components/Contacto.vue'

</script>
<template>
  <div class="main-content">

  <!-- <TopBar/> ----------------->
  <section>
    <div><TopBar/></div>
  </section>

  <!-- <Hero Image/> ----------------->
  <section>
    <div><HeroImage/></div>
  </section>
    
  <!-- <Servicios/> ----------------->
  <section>
    <div><Servicios/></div>
  </section>
    
  <!-- <Refacciones/> ----------------->
  <section>
    <div><Refacciones/></div>
  </section>
    
  <!-- <Contacto/> ----------------->
  <section>
    <div><Contacto/></div>
  </section>
    
  </div>
</template>
