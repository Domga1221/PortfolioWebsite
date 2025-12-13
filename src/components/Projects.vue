<template>
    <section class="relative py-20 overflow-hidden" id="projects">
        <div class="relatie z-10 max-w-7xl mx-auto px-4 sm:px-6 
        lg:px-8">
            <!-- Section Header -->
             <div class="text-center mb-16" data-aos='fade-up'>
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    My <span class="text-transparent bg-clip-text 
                    bg-linear-to-r from-rose-400 to-pink-400">
                    Projects
                </span>
                </h2>
                <p class="text-rose-200 text-lg max-w-2xl mx-auto">
                    A collection of my recent and older work. Make sure to click the eye or code bracket icons for demonstration videos
                    or the code on GitHub.
                </p>
            </div>

            <!-- Projects Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3
            gap-8">
                <div v-for="(project, index) in projects"
                :key="(project.id)"
                class="group relative bg-linear-to-br from-gray-800/50 
                to-rose-900/30 rounded-3xl overflow-hidden border
                backdrop-blur-sm hover:border-rose-400/40
                transition-all duration-500 hover:transform
                hover:-tranpink-y-2"
                :class="project.boardColor"
                data-aos="fade-up"
                :data-aos-delay="(index + 1) * 100"> 
                <div class="relative overflow-hidden">
                    <img 
                    :src="project.image"
                    :alt="project.title"
                    class="w-full h-48 object-cover group-hover:scale-110
                    transition-transform duration-500">
                    <div class="absolute inset-0 bg-linear-to-t 
                    from-gray-900 via-transparent to-transparent">
                    </div>
                    <div class="absolute top-4 right-4">
                        <span class="px-3 py-1 text-white text-xs
                        rounded-full font-semibold"
                        :class="project.badgeColor">
                        {{ project.category }}
                        </span>
                    </div>
                </div>
                <!-- Project Content -->
                 <div class="p-6">
                    <h3 class="text-xl font-bold text-white
                    group-hover:text-rose-400 transition-colors
                    duration-300">
                        {{ project.title }}
                    </h3>
                    <p class="text-rose-100 text-sm leading-relaxed
                    mb-4">
                        {{ project.dest }}
                    </p>
                    <!-- Technologies -->
                    <div class="flex flex wrap gap-2 mb-4">
                        <span v-for="tech in project.technology"
                        :key="tech"
                        class="px-2 py-1 border rounded text-xs"
                        :class="tech.class">
                            {{ tech.name }}
                        </span> 
                    </div>
                    <!-- Project Links -->
                     <div class="flex gap-3">
                        <a v-for="link in project.links"
                        :key="link.name"
                        :href="link.url"
                        target="_blank"
                        :class="link.class"
                        class="flex items-center gap-2 transition-colors
                        duration-300 text-sm font-medium">
                        <component :is="link.icon" class="w-8 h-8">
                            {{ link.name }}
                        </component>
                        </a>
                     </div>
                 </div>        
                </div>
            </div>

            <!-- CTA section -->
            <div class="text-center mt-16" data-aos="fade-up">
                <div class="inline-flex flex-col sm:flex-row gap-4
                items-center">
                <a href="https://github.com/Domga1221" target="_blank">
                    <button class="px-8 py-4 rounded-xl bg-linear-to-r 
                    from-rose-500 to-pink-500 text-white 
                    font-semibold hover:shadow-lg hover:shadow-rose-500/25
                    transition-all duration-300 hover:scale-105 
                    flex items-center">

                        <ArrowRightIcon class="w-5 h-5 ml-2"></ArrowRightIcon>
                        View all projects
                    </button>
                </a>
                    <!--
                    <button class="px-8 py-4 rounded-xl border-2
                    border-rose-400 text-rose-400 font-semibold
                    hover:bg-rose-400/10 transition-all duration-300
                    flex items-center">
                    <ChatBubbleLeftRightIcon class="w-5 h-5 mr-2"></ChatBubbleLeftRightIcon>
                    Discuss project
                    </button>
                    -->
                </div>
            </div>


        </div>

    </section>
</template>

<script setup>
import { ArrowRightIcon, ChatBubbleLeftRightIcon, ClockIcon, CodeBracketIcon, EyeIcon } from '@heroicons/vue/16/solid';
import { ref } from 'vue';


import project1 from '../../public/project1.png'
import project2 from '../../public/project2.png'
import project3 from '../../public/project3.jpg'
import project4 from '../../public/project4.png'
import project5 from '../../public/project5.png'
import project6 from '../../public/project6.png'


const projects = ref([
    {
        id: 1,
        title: "PBR Renderer & Editor",
        dest: 'Created in summer of 2023 for Advanced Computer Graphics course. Contains post-processing effects like color correction, bloom, SSAO, as well as particle systems.',
        image: project1,
        category: 'Graphics',
        boardColor: 'border-rose-500/20',
        badgeColor: "bg-rose-500",
        technology: [ 
            {
                name: "C/C++",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
            {
                name: "OpenGL",
                class: 'bg-pink-500/20 border-pink-400/30 text-pink-200'
            },
            {
                name: "Premake",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
        ],
        links: [
            {
                name: "Live Demo", url: "https://youtu.be/o7CtYwoZbIw?si=_OVHxUioG6yOYNT8", icon: EyeIcon,
                class: 'text-rose-400 hove:text-rose-300',
            },
            {
                name: "Code", url: "https://github.com/Domga1221/ResPublicaRomana", icon: CodeBracketIcon,
                class: 'text-pink-400 hove:text-pink-300',
            }
        ]
    },
    {
        id: 2,
        title: "Shader",
        dest: 'Created in summer of 2023 for Shaders course. Contains 3D as well as 2D shaders.',
        image: project2,
        category: 'Graphics',
        boardColor: 'border-pink-500/20',
        badgeColor: "bg-pink-500",
        technology: [ 
            {
                name: "OpenGL",
                class: 'bg-pink-500/20 border-pink-400/30 text-pink-200'
            },
        ],
        links: [
            {
                name: "Live Demo", url: "https://youtu.be/rGUGYqjVrn4?si=BUSul4CqR-RhxnMa", icon: EyeIcon,
                class: 'text-rose-400 hove:text-rose-300',
            },
            /*
            {
                name: "Code", url: "#", icon: CodeBracketIcon,
                class: 'text-pink-400 hove:text-pink-300',
            }
            */
        ]
    },
    {
        id: 3,
        title: "Games Coaching App",
        dest: 'Created in summer of 2021 for Android course. Addresses the problems of video game coaches, offering a platform which delivers their services to the end customer.',
        image: project3,
        category: 'Social',
        boardColor: 'border-rose-500/20',
        badgeColor: "bg-rose-500",
        technology: [ 
            {
                name: "Android Studio",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
            {
                name: "Express",
                class: 'bg-pink-500/20 border-pink-400/30 text-pink-200'
            },
            {
                name: "OkHttp",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
        ],
        links: [
            {
                name: "Code", url: "https://github.com/Domga1221/Games-Coaching-App-AndroidStudio", icon: CodeBracketIcon,
                class: 'text-rose-400 hove:text-rose-300',
            },
            /*
            {
                name: "Code", url: "#", icon: CodeBracketIcon,
                class: 'text-pink-400 hove:text-pink-300',
            }
            */
        ]
    },
    /*
    {
        id: 4,
        title: "Restaurant website",
        dest: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Baetae officiis perferendiis illo...',
        image: project4,
        category: 'restaurant',
        boardColor: 'border-rose-500/20',
        badgeColor: "bg-rose-500",
        technology: [ 
            {
                name: "React",
                class: 'bg-pink-500/20 border-pink-400/30 text-pink-200'
            },
            {
                name: "Socket.io",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
            {
                name: "PostgreSQL",
                class: 'bg-pink-500/20 border-pink-400/30 text-pink-200'
            },
        ],
        links: [
            {
                name: "Live Demo", url: "#", icon: EyeIcon,
                class: 'text-rose-400 hove:text-rose-300',
            },
            {
                name: "Code", url: "#", icon: CodeBracketIcon,
                class: 'text-pink-400 hove:text-pink-300',
            }
        ]
    },
    {
        id: 5,
        title: "portfolio website",
        dest: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Baetae officiis perferendiis illo...',
        image: project5,
        category: 'portfolio',
        boardColor: 'border-rose-500/20',
        badgeColor: "bg-rose-500",
        technology: [ 
            {
                name: "Vue.js",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
            {
                name: "Tailwind CSS",
                class: 'bg-pink-500/20 border-pink-400/30 text-pink-200'
            },
            {
                name: "AOS",
                class: 'bg-rose-500/20 border-rose-400/30 text-rose-200'
            },
        ],
        links: [
            {
                name: "Live Demo", url: "#", icon: EyeIcon,
                class: 'text-rose-400 hove:text-rose-300',
            },
            {
                name: "Code", url: "#", icon: CodeBracketIcon,
                class: 'text-pink-400 hove:text-pink-300',
            }
        ]
    },
    {
        id: 6,
        title: "Dashboard",
        dest: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Baetae officiis perferendiis illo...',
        image: project6,
        category: 'dashboard',
        boardColor: 'border-pink-500/20',
        badgeColor: "bg-pink-500",
        technology: [ 
            {
                name: "Dashboard",
                class: 'bg-gray-500/20 border-gray-400/30 text-gray-200'
            }
        ],
        links: [
            {
                name: "In Progress", url: "#", icon: ClockIcon,
                class: 'text-pink-400 hove:text-pink-300',
            }
        ]
    }
    */
])
</script>

<style>

</style>