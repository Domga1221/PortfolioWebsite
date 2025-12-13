<template>
  <section class="relative py-0 overflow-hidden" id="services">
    <div class="relative z-10 max-w-7-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center m-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                What <span class="text-transparent bg-clip-text bg-linear-to-r
                from-rose-400 to-pink-400">
                    I offer
                </span>

            </h2>
            <p class="text-rose-200 text-lg max-w-2xl mx-auto"
            data-aos="fade-up"
            data-aos-delay="100">
                During my study period and internship at Ravensburger, I have come in touch with various aspects of computer science and product development. 
                <br>
            </p>
            <p class="text-rose-200 text-3xl mx-auto">
            Click the cards to find out more...
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div v-for="(service, index) in services" :key="service.id"
            :data-aos="'fade-up'"
            :data-aos-delay="(index * 100) + 100"
            class="group relative p-8 rounded-2xl bg-linear-to-br 
            from-gray-800/50 to-rose-900/30 backdrop-blur-sm 
            border border-rose-500-20 hover:border-rose-400/40
            transition-all duration-500 hover:transform
            hover:-tranpink-y-2">
            <a :href="service.href" target="_blank">
            <div class="absolute inset-0 bg-linear-to-r from-rose-500/5
            to-pink-500/5 rounded-2xl opacity-0 duration-500 
            group-hover:opacity-100 transition-opacity"></div>
            <div class="relative z-10 mb-6">
                <div class="inline-flex items-center justify-center
                w-16 h-16 rounded-xl bg-linear-to-r from-rose-500/20
                to-pink-500/20 border border-rose-400/30 
                group-hover:scale-110 transition-transform 
                duration-300">
                    <component
                    :is="service.icon"
                    class="w-8 h-8 text-rose-400"></component>

                </div>
            </div>
            <div class="relative z-10">
                <h3 class="text-xl font-bold text-white mb-3 
                group-hover:text-rose-400 transition-colors
                duration-300">
                    {{ service.name }}
                </h3>
                <p class="text-rose-100 leading-relaxed">
                    {{ service.desc }}
                </p>
            </div>
            <div class="absolute bottom-6 right-6 opacity-0 
            group-hover:opacity-100 transform tranpink-x-4
            group-hover:tranpink-x-0 transition-all duration-300">
                <ArrowRightIcon class="w-6 h-6 text-pink-400"></ArrowRightIcon>
            </div>
            </a>
            </div>
        </div>
        <div class="text-center mt-8"
        >
        <!-- data-aos="fade-up"
        data-aos-delay="100" -->
            <div class="inline-flex flex-col sm:flex-row gap-4 
            items-center">
            <a href="#contact">
                <button class="px-8 py-4 rounded-xl border-2
                border-rose-400 text-rose-400 font-semibold 
                hover:bg-rose-400/10 transition-all duration-300
                flex items-center">
                Get In Touch
                <ChatBubbleLeftRightIcon class="w-5 h-5 ml-2"></ChatBubbleLeftRightIcon>
            </button>
            </a>
            </div>
        </div>
    </div>
  </section>
</template>

<script setup>
import { ArrowRightIcon, ChatBubbleLeftRightIcon, CodeBracketIcon, ComputerDesktopIcon, DevicePhoneMobileIcon, 
    DocumentTextIcon, EnvelopeIcon, PaintBrushIcon } 
    from '@heroicons/vue/16/solid';
import { ref } from 'vue';

const services = ref([
    {
        id: 1,
        icon: CodeBracketIcon,
        name: 'Development',
        desc: 'My course of study is computer science with a focus on graphics. Hence why I have a lot of experience in developing prototypes for games or smaller graphics applications. Also I worked a lot on frontends and backends as well as Android apps.',
        href: "https://github.com/Domga1221"
    },
    {
        id: 2,
        icon: DocumentTextIcon,
        name: 'Writing & Content Creation',
        desc: 'During my time at Ravensburger I worked with game design documents to create the vision of the designer as closely as possible in media. In my free time I create content on YouTube on video games and more...',
        href: "https://www.youtube.com/@domga8461"
    },
    {
        id: 5,
        icon: PaintBrushIcon,
        name: '3D Design',
        desc: 'In my free time I work on 3D projects, some of which you have seen on this website already.',
        href: "https://www.artstation.com/domga"
    },
    /*
    {
        id: 3,
        icon: DevicePhoneMobileIcon,
        name: 'Mobile Delopment',
        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Baetae officiis perferendiis illo...'
    },
    {
        id: 4,
        icon: EnvelopeIcon,
        name: 'Email Marketing',
        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Baetae officiis perferendiis illo...'
    },
    {
        id: 6,
        icon: ComputerDesktopIcon,
        name: 'Web Design',
        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Baetae officiis perferendiis illo...'
    }
    */
])
</script>

<style>

</style>