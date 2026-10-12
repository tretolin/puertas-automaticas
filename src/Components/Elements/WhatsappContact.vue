<script setup>
const link = "https://wa.link/0th1dw";
</script>
<template>
    <a :href="link">
        <div
            class="whatsapp flex pl-1 text-white text-[13px] w-50 rounded-2xl items-center justify-center py-0 px-0 overflow-hidden min-w-[120px]"
        >
            <img
            src="../../../public/assets/images/whatsapp-logo.svg"
            width="30"
            alt="WhatsApp Logo"
            />
            <div class="text-[13px] w-50">Cotizar por WhatsApp</div>
        </div>
    </a>
</template>
<style>
.whatsapp {
    background-color: #25D366;
}
</style>