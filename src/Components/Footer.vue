<script setup>
import { ref } from 'vue';
const words = ref(["Puertas","Refacciones", "Mantenimiento", 'Monterrey, NL']);
</script>
<template>
    <div class="footer flex justify-between p-4">
        <!-- LEFT -->
        <div class="left">
            <div class="brand-logo">
                <img
                    src="../../public/assets/images/AFA-AUT.svg"
                    width="130"
                    alt="Brand Logo"
                />
            </div>
        </div>

        <!-- CENTER -->
        <div class="center">
            <div>
                <div class="px-4 inline border-r text-gray-200 border-gray-200" v-for="(word, index) in words">
                    {{ word }}
                </div>
            </div> 
        </div>

        <!-- RIGHT -->
        <div class="right flex">
        
            <div class="icon-container text-center px-4">
                <!-- Instagram icon -->
                <div class="inline">
                    <img src="../../public/assets/images/ig_icon.svg" width="22px" alt="instagram"/>
                </div>
            </div>

            <!-- Facebook icon -->
                <div class="inline">
                    <img src="../../public/assets/images/fb-icon.svg" width="22px" alt="Facebook"/>
                </div>

            <div class="text-sm pl-4">Síguenos en nuestras redes</div>

        </div>


        
    </div>
    <div class="text-center text-gray-600 py-1 border-t border-gray-800"> AFA - Siempre en movimiento</div>
</template>