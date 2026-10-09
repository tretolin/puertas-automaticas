<script setup>

import { onMounted } from "vue"
import { ref } from "vue"

onMounted(() => {
    console.log("ServicioBaner mounted")
    // icon.value = props.icon
})
const getImage = (icon) => {
    return `../../assets//images/${icon}.svg`
}

const props = defineProps({
    description: {
        type: String,
        required: true
    },
    icon: {
        type: String,
        required: true
    },
})
</script>

<template>
    <div  class="mt-6 flex w-37.5 border-r-3 border-gray-700 last:border-r-0 mx-2">
        <div class="flex align-middle pr-1">
            <img
                :src="getImage(icon)"
                alt="servicio"
                class="h-12.5"
            />
        </div>
        <div class="text-[.8rem] mt-1 flex items-center justify-center ">{{ description }}</div>
    </div>
</template>