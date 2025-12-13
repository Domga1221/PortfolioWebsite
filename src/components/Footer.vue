<template>
    <footer class="relative bg-gray-900/80 border-t
    border-rose-500/20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 py-12">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- Brand -->
                <div class="md:col-span-2">
                    <div class="text-2xl font-bold bg-linear-to-r
                    from-rose-400 to-pink-400 bg-clip-text 
                    text-transparent
                    mb-4">
                    Kind regards, Dominik
                </div>
                <p class="text-rose-200 text-sm leading-relaxed max-w-md">
                    Thank you for visiting my web portfolio!
                </p>
                <div class="flex gap-4 mt-6">
                <a class="p-2 bg-rose-500/20
                    border border-rose-400/30 rounded-lg
                    text-rose-400 hover:bg-rose-500/30
                    transition-all">
                    <FaceSmileIcon class="w-5 h-5"></FaceSmileIcon>
                </a>
                <a class="p-2 bg-rose-500/20
                    border border-rose-400/30 rounded-lg
                    text-rose-400 hover:bg-rose-500/30
                    transition-all">
                    <HandThumbUpIcon class="w-5 h-5"></HandThumbUpIcon>
                </a>
                <a class="p-2 bg-rose-500/20
                    border border-rose-400/30 rounded-lg
                    text-rose-400 hover:bg-rose-500/30
                    transition-all">
                    <HeartIcon class="w-5 h-5"></HeartIcon>
                </a>
                </div>

                </div>

                <!-- Quick Links -->
                <div>
                    <h3 class="text-white font-semibold mb-4">
                        Quick Links
                    </h3>
                    <ul class="space-y-2">
                        <li v-for="link in quickLinks"
                        :key="link.name">
                        <a
                        :href="link.href"
                        class="text-rose-200 hover:text-rose-400
                        text-sm transition-colors">
                        {{ link.name }}
                        </a>
                        </li>
                    </ul>
                </div>

                <!-- Bottom Bar -->

                <div class=" flex
                flex-col md:flex-row justify-between items-center">
                    <p class="text-rose-300 text-sm">
                        @2026 Dominik. All rights reserved 
                    </p>

                </div>

            </div>
        </div>
    </footer>
</template>

<script setup>
import { FaceSmileIcon, HandThumbUpIcon, HeartIcon } from '@heroicons/vue/24/solid';

const quickLinks = [
    {name: "Home", href: "#home"},
    {name: "About", href: "#about"},
    {name: "Services", href: "#services"},
    {name: "Projects", href: "#projects"},
    {name: "Contact", href: "#contact"},
]

const services = [
    'Web Development',
    'Mobile Development',
    'UI/UX Design',
    'Technical Writing',
    'Consultation'
]

</script>

<style>

</style>