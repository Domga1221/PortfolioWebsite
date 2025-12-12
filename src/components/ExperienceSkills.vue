<template>
  <section class="relative py-20 overflow-hidden" id="skills">
    <div class="relative z-10 max-w-6xl mx-auto
     px-4 sm:px-6 lg:px-8">
    
        <div class="text-center mb-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                <span class="text-transparent bg-clip-text 
                bg-linear-to-r from-rose-400 to-pink-400">
                    Skills 
                </span>& Experience
            </h2>
            <!-- 
            <p class="text-rose-200 text-lg max-w-2xl mx-auto">
                my technical expertise and professional journey
            </p> 
            -->
            <div class="grid lg:grid-cols-2 gap-12 lg:gap-16">
                <div data-aos="fade-right">
                    <h3 class="text-xl font-bold text-white mb-8 flex
                    items-center gap-3 mt-10">
                    <LanguageIcon class="w-6 h-6 text-pink-400">
                    </LanguageIcon>
                        Languages
                    </h3>
                    <div class="space-y-6"> 
                        <div 
                        v-for="skill in skills"
                        :key="skill.id"
                        class="group"> 
                            <div class="flex items-center justify-between 
                            mb-3">
                                <span class="text-rose-200 font-semibold 
                                flex items-center gap-2"> 
                                    <component 
                                    :is="skill.icon"
                                    class="w-5 h-5"
                                    :class="skill.iconColor"></component>
                                    {{ skill.title }}
                                </span>
                                <span class="text-white skill.percentageColor">
                                    {{ skill.percentage }}
                                </span>
                            </div>
                            <div class="h-2 bg-gray-700 rounded-full
                            overflow-hidden">
                            <div class="h-full rounded-full transition-all
                            duration-1000 group-hover:scale-105"
                            :class="skill.gradient"
                            :style="{width: skill.percentage + '%'}"> 
                                
                            </div>
                            </div>
                            
                        </div>
                    </div>
                </div>

                <div class="mt-10">
                    <h4 class="text-xl font-bold text-white mb-6 
                    flex items-center gap-2">
                    <Squares2X2Icon class="w-6 h-6 text-pink-400">
                    </Squares2X2Icon>
                    Tech Stack
                </h4> 
                <div class="flex flex-wrap gap-3"> 
                    <span v-for="tech in techStack"
                    :key="tech"
                    class="px-4 py-2 bg-linear-to-r from-rose-500/20
                    border border-rose-400/30 rounded-full
                    text-rose-200 text-sm font-medium
                    hover:scale-105 transition-transform 
                    duration-300">
                    {{ tech }}
                    </span>
                </div>
                <h3 class="text-l font-bold text-white mt-4 mb-8">Scrap the above, just use C and NVIM for everything</h3>
                </div>
            </div>
            <div data-aos="fade-left"> 
                <h3 class="text-2xl font-bold text-white mb-8
                flex items-center gap-3 mt-10">
                <BriefcaseIcon class="w-8 h-8 text-pink-400"></BriefcaseIcon>
                Work Experience & Studies
                </h3>
                <div class="space-y-8">
                    <div v-for="exp in experiences"
                    :key="exp.id"
                    class="relative pl-8 border-l-2 group"
                    :class="exp.borderColor"> 
                    <div class="absolute -left-2 top-0 w-4 h-4 rounded-full
                    group-hover:scale-150 transition-transform 
                    duration-300"
                    :class="exp.dotColor">   
                    </div>
                    <div class="bg-linear-to-br from-gray-800/50 
                    to-rose-900/30 rounded-2xl p-6 border 
                    backdrop-blur-sm group-hover:border-rose-400/40 
                    transition-all duration-300"
                    :class="exp.borderClass">
                    <div class="flex flex-col sm:flex-row sm:items-center 
                    sm:justify-between mb-3">
                    <h4 class="text-lg font-bold text-white"> 
                        {{ exp.position }}
                    </h4>
                    <span :class="exp.dateColor" 
                    class="mt-1 sm:mt-0">
                    {{ exp.period }}
                    </span>
                    <p class="font-medium"
                    :class="exp.companyColor">
                        {{ exp.company }}
                    </p>
                    <p class="text-rose-100 text-sm leading-relaxed">
                        {{ exp.desc }}
                    </p>

                    </div> 

                    </div>

                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script setup>
import { BriefcaseIcon, CurrencyPoundIcon, CurrencyYenIcon, FlagIcon, LanguageIcon, Squares2X2Icon } from '@heroicons/vue/16/solid';

const skills = [
    {
        id: 1, 
        title: "German",
        icon: FlagIcon,
        iconColor: 'text-rose-400',
        percentage: 100,
        percentageColor: "text-rose-400 text-sm",
        gradient: 'bg-linear-to-r from-pink-500 to-pink-500'
    },
    {
        id: 2, 
        title: "English",
        icon: CurrencyPoundIcon,
        iconColor: 'text-rose-400',
        percentage: 80,
        percentageColor: "text-rose-400 text-sm",
        gradient: 'bg-linear-to-r from-rose-500 to-pink-500'
    },
    {
        id: 3, 
        title: "Japanese",
        icon: CurrencyYenIcon,
        iconColor: 'text-rose-400',
        percentage: 40,
        percentageColor: "text-rose-400 text-sm",
        gradient: 'bg-linear-to-r from-rose-500 to-pink-500'
    },
    /*
    {
        id: 4, 
        title: "Mobile Development",
        icon: DevicePhoneMobileIcon,
        iconColor: 'text-pink-400',
        percentage: 80,
        percentageColor: "text-pink-400 text-sm",
        gradient: 'bg-linear-to-r from-rose-500 to-pink-500'
    },
    {
        id: 5, 
        title: "DevOps & Cloud",
        icon: DevicePhoneMobileIcon,
        iconColor: 'text-pink-400',
        percentage: 75,
        percentageColor: "text-pink-400 text-sm",
        gradient: 'bg-linear-to-r from-rose-500 to-pink-500'
    },
    */
]

const experiences = [
    {
        id: 1,
        position: "Computer Science Master Studies",
        company: "Ravensburg Weingarten University",
        period: "2023 - now",
        desc: "With focus on games and computer graphics",
        borderColor: "border-rose-500/30",
        dotColor: "bg-rose-500",
        borderClass: "border-rose-500/20",
        dateColor: "text-rose-400 text-sm font-semibold",
        companyColor: "text-pink-400",
    },
    {
        id: 2,
        position: "Internship in Board Games",
        company: "Ravensburger",
        period: "2022", 
        desc: "Working on board games with audio and digital toys, innovation branch",
        borderColor: "border-rose-500/30",
        dotColor: "bg-rose-500",
        borderClass: "border-rose-500/20",
        dateColor: "text-rose-400 text-sm font-semibold",
        companyColor: "text-pink-400",
    },
    {
        id: 3,
        position: "Applied Computer Science Studies",
        company: "Ravensburg Weingarten University",
        period: "2018 - 2023", 
        desc: "With focus on games and media",
        borderColor: "border-rose-500/30",
        dotColor: "bg-rose-500",
        borderClass: "border-rose-500/20",
        dateColor: "text-rose-400 text-sm font-semibold",
        companyColor: "text-pink-400",
    }
]

const techStack = [
    'C++', 'C#', 'Python', 'Java',
    'Vue js', 'React', 'TypeScript', 'Node js', 'Express',
    'MySQL', 'Android Studio'
]
</script>

<style>

</style>