<script setup>
import WhatsappContact from './Elements/WhatsappContact.vue';
import PhoneCallButton from './Elements/PhoneCallButton.vue';
</script>
<template>
    <section class="w-full bg-[#070e17] text-white py-8 px-4 font-sans">
    <div
        class="max-w-7xl mx-auto flex flex-col lg:flex-row items-stretch border-gray-800"
    >
        <!-- Sección Izquierda: Ubicación, Horarios y Mapa -->
        <div
        class="flex-1 flex flex-col md:flex-row items-center justify-between gap-6 p-6 lg:border-r border-gray-700/60"
        >
        <!-- Datos de contacto (Ubicación y Horarios) -->
        <div class="flex flex-col gap-6 w-full md:w-1/2">
            <!-- Ubicación -->
            <div class="flex items-start gap-3">
            <div class="text-blue-500 mt-1 flex-shrink-0">
                <!-- Icono Ubicación -->
                <svg class="w-7 h-7 fill-current" viewBox="0 0 24 24">
                <path
                    d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"
                />
                </svg>
            </div>
            <div>
                <h3
                class="text-xs font-bold text-gray-300 uppercase tracking-wider"
                >
                Ubicación
                </h3>
                <p class="text-sm font-semibold text-white mt-0.5">
                Monterrey, Nuevo León, México
                </p>
                <p class="text-xs text-gray-400 mt-1">
                Estamos listos para atenderte. ¡Visítanos o contáctanos!
                </p>
            </div>
            </div>

            <!-- Horarios -->
            <div class="flex items-start gap-3">
            <div class="text-blue-500 mt-1 flex-shrink-0">
                <!-- Icono Reloj -->
                <svg class="w-7 h-7 fill-current" viewBox="0 0 24 24">
                <path
                    d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm.5-13H11v6l5.2 3.2.8-1.3-4.5-2.7V7z"
                />
                </svg>
            </div>
            <div>
                <h3
                class="text-xs font-bold text-gray-300 uppercase tracking-wider"
                >
                Horarios de Atención
                </h3>
                <p class="text-xs text-gray-300 mt-1">
                Lunes a Viernes:
                <span class="text-gray-400">8:00 a.m. - 6:00 p.m.</span>
                </p>
                <p class="text-xs text-gray-300">
                Sábados:
                <span class="text-gray-400">8:00 a.m. - 2:00 p.m.</span>
                </p>
            </div>
            </div>
        </div>

        <!-- Mapa miniatura -->
        <div class="w-full md:w-1/2 flex justify-center md:justify-end">
            <div
            class="relative w-full max-w-[200px] h-36 rounded-xl overflow-hidden border border-gray-600/50 shadow-lg"
            >
            <!-- Imagen estática del mapa o iframe de Google Maps -->
            <img
                src="@/assets/images/monterrey-maps-gps.png"
                alt="Mapa Monterrey"
                class="w-full h-full object-cover"
            />
            <!-- Pin y etiqueta sobre el mapa -->
            <div
                class="absolute inset-0 flex flex-col items-center justify-center bg-black/10 pointer-events-none"
            >
                <div
                class="bg-white/90 text-black text-[11px] font-bold px-2 py-0.5 rounded shadow mt-10"
                >
                Monterrey
                </div>
            </div>
            </div>
        </div>
        </div>

        <!-- Sección Derecha: Cotización y Llamados a la Acción -->
        <div
        class="flex-1 relative flex flex-col justify-center p-6 bg-cover bg-center overflow-hidden"
        style="
            background-image:
            linear-gradient(
                to right,
                rgba(7, 14, 23, 0.95),
                rgba(7, 14, 23, 0.75)
            ),
            url(&quot;https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&w=800&q=80&quot;);
        "
        >
        <div class="flex flex-col items-start gap-2 max-w-lg">
            <!-- Subtítulo con acento azul -->
            <div class="flex items-center gap-2">
            <span class="w-6 h-1 bg-blue-500 rounded-full"></span>
            <span
                class="text-xs font-semibold text-gray-300 uppercase tracking-wider"
                >¿Necesitas una cotización?</span
            >
            </div>

            <!-- Título principal -->
            <h2
            class="text-2xl md:text-3xl font-black text-white uppercase tracking-wide"
            >
            ¡Contáctanos!
            </h2>

            <!-- Descripción -->
            <p class="text-xs md:text-sm text-gray-300 mb-2">
            Estamos para ayudarte con cualquier consulta o proyecto.
            </p>

            <!-- Botones de Acción -->
            <div class="flex flex-wrap items-center gap-3 w-full mt-1">
            <!-- Botón WhatsApp -->
            <WhatsappContact/>
            <!-- Botón Llamar -->
            <PhoneCallButton/>
            </div>
            <div>
            
            </div>

        </div>
        </div>
    </div>
    </section>
</template>
