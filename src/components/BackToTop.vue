<template>
    <button v-if="isVisible" @click="scrollToTop"
    class="fixed bottom-4 right-4 bg-linear-to-r from-rose-600
    to-pink-600 text-white rounded-full w-12 h-12 items-center 
    justify-center text-xl cursor-pointer transition-opacity 
    duration-opacity duration-300 hover:bg-rose-600"
    >
        <ArrowUpIcon/>
    </button>
</template>

<script setup>
import { ArrowUpIcon } from '@heroicons/vue/16/solid';
import { handleError, onMounted, onUnmounted, ref } from 'vue';

const isVisible = ref(false);

const handleScroll = ()=> {
    isVisible.value = window.scrollY > 300;
}
const scrollToTop = () => {
    window.scrollTo({top:0, behavior:'smooth'});
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
})

</script>

<style>

</style>