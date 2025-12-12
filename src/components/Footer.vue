<template>
    <footer class="relative bg-gray-900/80 border-t
    border-blue-500/20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 py-12">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- Brand -->
                <div class="md:col-span-2">
                    <div class="text-2xl font-bold bg-linear-to-r
                    from-blue-400 to-cyan-400 bg-clip-text 
                    text-transparent
                    mb-4">
                    Mary.dev
                </div>
                <p class="text-blue-200 text-sm leading-relaxed max-w-md">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Baetae officiis perferendiis illo...
                </p>
                <div class="flex gap-4 mt-6">
                <a href="#" class="p-2 bg-blue-500/20
                    border border-blue-400/30 rounded-lg
                    text-blue-400 hover:bg-blue-500/30
                    transition-all">
                    <EnvelopeIcon class="w-5 h-5"></EnvelopeIcon>
                </a>
                <a href="#" class="p-2 bg-blue-500/20
                    border border-blue-400/30 rounded-lg
                    text-blue-400 hover:bg-blue-500/30
                    transition-all">
                    <PhoneIcon class="w-5 h-5"></PhoneIcon>
                </a>
                <a href="#" class="p-2 bg-blue-500/20
                    border border-blue-400/30 rounded-lg
                    text-blue-400 hover:bg-blue-500/30
                    transition-all">
                    <MapPinIcon class="w-5 h-5"></MapPinIcon>
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
                        class="text-blue-200 hover:text-blue-400
                        text-sm transition-colors">
                        {{ link.name }}
                        </a>
                        </li>
                    </ul>
                </div>

                <!-- Bottom Bar -->

                <div class=" flex
                flex-col md:flex-row justify-between items-center">
                    <p class="text-blue-300 text-sm">
                        @2026 Dominik. All rights reserved 
                    </p>

                </div>

            </div>
        </div>
    </footer>
</template>

<script setup>
import { EnvelopeIcon, MapPinIcon, PhoneIcon } from '@heroicons/vue/24/outline';

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