<script setup>

const props = defineProps({
    title: {
        type:String,
        required: false
    },
    icon: {
        type: String,
        required: false},
    description:{
        type:String,
        required: false
    }
})

const getImage = (icon) => {
    console.log(icon, '')
    return `../../assets/images/${icon}.svg`
}

</script>

<template>
    <div class="flex-1 border-r border-gray-300">
        <div class="servicio-item  text-center">
            <div class="icon w-full flex justify-center px-2">
                <div class=" h-12 w-12 rounded-full bg-blue-100 flex justify-center p-2 mb-2">
                    <img :src="getImage(icon)"/>
                </div>
            </div>
            <div class="font-bold text-center pb-2 px-2">
                {{ title}}
            </div>
            <div> {{ description}}</div>
        </div>
    </div>
</template>