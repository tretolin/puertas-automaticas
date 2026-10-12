<script setup>
import ServicioItem from './Elements/ServicioItem.vue';
import { ref } from "vue"

const servicios = ref([
    {
        icon:'tool',
        title:'Instalación de puertas automáticas',
        description:"Residenciales, comerciales e industrias"
    },
    {
        icon:'fixes',
        title:'Reparación y mantenimiento',
        description:"Diagnóstico y solución de fallas"
    },
    {
        icon:'automation',
        title:'Automatización de puertas',
        description:"Moderniza y haz seguro tu espacio"
    },
    {
        icon:'search',
        title:'Diagnóstico de fallas',
        description:"Detectamos y reparamos el problema"
    },
    {
        icon:'package',
        title:'Venta e instalación de motores y accesorios',
        description:"Las mejores marcasy garantía"
    },
])

</script>

<template>
    <div class="bg-white flex text-center justify-center text-gray-800 pt-4 pb-4">
        <div class="">
            <!-- Título de servicios -->
            <div>
                <div>
                    <div class="text-3xl font-bold uppercase text-blue-400 inline">—</div>
                    <div class="text-md font-bold uppercase inline pl-0 mt-3 text-gray-800">
                        Nuestros
                    </div>
                </div>
                <div class="text-3xl font-bold uppercase inline text-gray-800">Servicios</div>
            </div>

        <p class="text-sm text-gray-800 w-[80vw] text-[12px]">
            Brindamos soluciones completas para que tus puertas automáticas
            funcionen de manera óptima. Contamos con un equipo de expertos en
            instalación, mantenimiento y reparación de puertas automáticas para
            hogares, comercios, industrias y corporativos. funcionen al 100%
        </p>
        </div>
    </div>

    <!-- Estructura de las opciones -->

<div class="flex flex-col md:flex-row w-full bg-white text-gray-800 text-[12px] pb-4">
    <div class="flex-1 px-4">
        <div class="flex flex-col md:flex-row divide-y divide-gray-300 md:divide-y-0 md:divide-x">
            <ServicioItem
                v-for="(servicio, index) in servicios"
                :key="index"
                :title="servicio.title"
                :description="servicio.description"
                :icon="servicio.icon"
            />
        </div>
    </div>
</div>
</template>

<style>
.servicio-item {
    display: flex;
    flex-direction: column;
    line-height: 12px;
    /* font-weight: bold; */
}
</style>