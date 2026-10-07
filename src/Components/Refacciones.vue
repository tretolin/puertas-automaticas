<script setup>
import { ref } from "vue";
import RefactionItem from "./Elements/RefactionItem.vue";

const refacciones = ref([
  {
    title: "Tornillo",
    image: "pieza.jpg",
  },
  {
    title: "Motores",
    image: "motor.jpg",
  },
  {
    title: "Placa",
    image: "pieza.jpg",
  },
  {
    title: "Accesoorios y componentes",
    image: "motor.jpg",
  },
  {
    title: "Pila",
    image: "pieza.jpg",
  },
  {
    title: "Motores",
    image: "motor.jpg",
  },
]);

const description =
  "Contamos con una amplia variedad de refacciones para todo tipo de puertas automáticas. Trabajamos con las mejores marcas y garantizamos la calidad de cada producto.";
</script>
<template>
  <!-- Contenedor Principal -->
  <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 bg-slate-950 p-8">
    <!-- Columna Izquierda (Texto / Contenido) - 1/3 -->
    <div class="flex flex-col justify-between gap-6 lg:col-span-1">
      <div class="flex flex-col gap-4">
        <div class="flex items-center gap-2">
          <div>
            <div>
              <div class="text-3xl font-bold uppercase text-blue-400 inline">
                —
              </div>
              <div class="text-md font-bold uppercase inline pl-0 mt-3">
                Venta de
              </div>
            </div>
            <div class="text-3xl font-bold uppercase inline">Refacciones</div>
          </div>
        </div>
        <div class="pb-4">
          {{ description }}
          <div>
            <!-- Ver todas las refacciones button -->
            <div class="pt-4">
                <div class="inline-flex border border-sky-500 rounded-xl px-2 py-2">
                    Ver todas las refacciones &rarr;
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Columna Derecha (Grid de Tarjetas) - 2/3 -->
    <div class="lg:col-span-2">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
        <RefactionItem
          v-for="(refaction, index) in refacciones"
          :key="index"
          :title="refaction.title"
          :image="refaction.image"
        />
      </div>
    </div>
  </div>
</template>