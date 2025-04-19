<script setup>
import { onMounted, ref } from 'vue';
const animate = ref(false);
onMounted(() => {
    setTimeout(()=>{
        animate.value = true
    },0);
});
</script>
<template>
    <div class="absolute bottom-1/2 translate-y-1/2 right-1/2 translate-x-1/2">

        <div class="text-8xl text-nowrap font-bold">
            <a href="https://laravel.com/docs/12.x" class="text-red-500">Laravel</a> + 
            <a href="https://vuejs.org/guide/introduction.html" class="text-green-500">Vue</a> + 
            <a href="https://inertiajs.com/" class="text-purple-500">Inertia</a>
        </div>
        <div :class="['p-1 w-0 bg-slate-600 ease-in-out duration-500 transition-all rounded-4xl', {
            '!w-3/4':animate
        }]"></div>

        <p class="text-4xl">Now create something amazing 🚀</p>
    </div>
</template>
<style></style>