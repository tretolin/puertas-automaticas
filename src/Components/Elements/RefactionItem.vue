<script setup>
const props = defineProps({
    title: {
        type: String,
        required: true
    },
    image: {
        type: String,
        required: true
    }
})

const backgroundImage = () => {
    const path = `/../../public/assets/images/gallery/${props.image}`
    // const image = images[path]

    return {
        backgroundImage: `url(${path})`
    }
}
</script>

<template>
    <div
        class="flex flex-col flex-1 bg-slate-900 rounded-lg overflow-hidden"
    >
        <div
            class="producto h-32"
            :style="backgroundImage()"
        >
        </div>

        <div class="p-3 text-center text-white text-[12px]">
            {{ title }}
        </div>
    </div>
</template>

<style>
.producto {
    background-position: center;
    background-repeat: no-repeat;
    background-color: white;
    background-size: contain;
}
</style>