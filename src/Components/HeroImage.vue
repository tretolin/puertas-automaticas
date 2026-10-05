<script setup>
import WhatsappButton from "../Components/Elements/WhatsappContact.vue";
import PhoneCallButtonn from "../Components/Elements/PhoneCallButton.vue";
import ServicioBaner from "../Components/Elements/servicioBaner.vue";
</script>

<template>
<div class="home-hero px-8 pt-6 pb-4">
    <div class="hero-content">
    <div class="flex">
        <div class="text-4xl font-bold uppercase text-blue-400 inline">—</div>
        <div class="text-xl font-bold uppercase inlinw pl-2 mt-3">
        soluciones en
        </div>
    </div>
    <h1 class="text-5xl font-bold uppercase">Puertas</h1>
    <div class="text-5xl font-bold uppercase text-blue-400">Automáticas</div>
    <p class="text-lg mt-4 text-gray-300 w-[400px]">
        Venta, instalación, mantenimiento y relaciones de puertas automáticas
        para hogares, comercios, industrias y corporativos.
    </p>

    <!-- Botones de contacto -->
    <div class="mt-6 flex">
        <WhatsappButton class="mr-4" />
        <PhoneCallButtonn />
        <!-- <div class="flex border-1 border-white rounded-2xl px-2 items-center justify-center py-0 px-0 overflow-hidden">
            <img src="@/assets/images/phone.svg" alt="llamar" width="24" height="20" class="w-6 h-6 mr-2 mt-1" />
            <div class="text-sm">Llamar ahora</div>
        </div> -->
    </div>

    <!-- Servicio y ubicación -->
    <!-- <div class="mt-6 flex w-[150px]">
        <div class="flex align-middle pr-1">
            <img src="@/assets/images/verified.svg" alt="servicio" class="h-[50px]"  />
        </div>
        <div class="text-sm mt-1 flex items-center justify-center ">Servicio profesional</div>
    </div> -->
    <div class="flex">
        <ServicioBaner description="Servicio profesional" icon="verified"/>
        <ServicioBaner description="Atención rápida y confiable" icon="schedule"/>
        <ServicioBaner description="Monterrey, NL" icon="gps" />
    </div>
    </div>
</div>
</template>

<style scoped>
.home-hero {
position: relative;

background-image: url("@/assets/images/portada.jpg");
background-size: cover;
background-position: center;
}
</style>
