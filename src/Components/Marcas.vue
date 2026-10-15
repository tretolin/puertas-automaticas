<script setup>
import { ref } from 'vue';
const brands = ref(['horton', 'stanley', 'manusa', 'besam','dormakaba']);
</script>

<template>
    <div class="bg-white">
    <div class="bg-white flex text-center justify-center text-gray-800 pt-4 pb-0 border-t border-gray-200">
        <div class="">
            <!-- Título de servicios -->
            <div>
                <div>
                    <div class="text-3xl font-bold uppercase text-blue-400 inline">—</div>
                    <div class="text-md font-bold uppercase inline pl-0 text-gray-800">
                        Las mejores marcas
                    </div>
                </div>
            </div>
                    <p class="text-sm text-gray-800 w-[80vw] text-[12px]">
            Mantenemos las mejores marcas de puertas automáticas
        </p>
        </div>



    </div>
        <!-- </div> -->
        <div class="flex flex-wrap items-center justify-center gap-3 pb-2 w-full bg-white">
            <img
                v-for="(brand, index) in brands"
                :key="index"
                :src="`/assets/images/marcas/${brand}.jpg`"
                :alt="`Marca ${brand}`"
                class="w-auto h-auto max-w-full max-h-20 object-contain"
            />
        </div>
    </div>
</template>
