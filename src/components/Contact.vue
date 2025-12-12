<template>
    <section class="relative py-20 overflow-hidden" id="contact"> 
        <div class="relative z-10 max-w-4xl mx-auto px-4 sm:px-6 
        lg:px-8">
        <div class="text-center m-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white
            mb-4">
                Get In <span class="text-transparent bg-clip-text 
                bg-linear-to-r from-rose-400 to-pink-400"> 
                Touch
                </span>

            </h2>
            <p class="text-rose-200 text-lg">
              Let's work together!
            </p>

        </div>

        <div class="grid lg:grid-cols-2 gap-12">
            <!-- Contact Info -->
             <div data-aos="fade-right">
                <h3 class="text-2xl font-bold text-white 
                mb-6"> Contact Information
                </h3> 
                <div class="space-y-6">
                    <div class="flex items-center gap-4">
                        <EnvelopeIcon class="w-6 h-6 text-rose-400"></EnvelopeIcon>
                        <div>
                            <p class="text-white font-semibold">Email</p>
                            <p class="text-rose-200">domgalp@gmail.com</p>
                        </div>
                    </div>
                    <!-- 
                    <div class="flex items-center gap-4">
                        <PhoneIcon class="w-6 h-6 text-rose-400"></PhoneIcon>
                        <div>
                            <p class="text-white font-semibold">Phone</p>
                            <p class="text-rose-200">+1 555 123-4567</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <MapPinIcon class="w-6 h-6 text-rose-400"></MapPinIcon>
                        <div>
                            <p class="text-white font-semibold">Location</p>
                            <p class="text-rose-200">City, CA</p>
                        </div>
                    </div>
                    -->
                </div>

                <!--
                <div class="mt-8"> 
                    <h4 class="text-lg font-bold text-white mb-4">
                        Follow Me
                    </h4>
                    <div class="flex gap-4">
                        <a href="#"
                        class="p-3 bg-rose-500/20 border
                        border-rose-400/30 rounded-xl text-rose-400
                        hover:bg-rose-500/30 transition-all">
                            <ChatBubbleLeftRightIcon class="w-5 h-5"></ChatBubbleLeftRightIcon>
                        </a>
                        <a href="#"
                        class="p-3 bg-rose-500/20 border
                        border-rose-400/30 rounded-xl text-rose-400
                        hover:bg-rose-500/30 transition-all">
                            <UserGroupIcon class="w-5 h-5"></UserGroupIcon>
                        </a>
                        <a href="#"
                        class="p-3 bg-pink-500/20 border
                        border-pink-400/30 rounded-xl text-pink-400
                        hover:bg-pink-500/30 transition-all">
                            <ShareIcon class="w-5 h-5"></ShareIcon>
                        </a>
                    </div>
                </div>
                -->
             </div>

             <!-- Contact Form -->
              <!--
              <div data-aos="fade-left"> 
                <form class="space-y-6">
                    <div class="grid sm:grid-cols-2 gap-6"> 
                        <div> 
                            <label class="text-white text-sm 
                            font-medium mb-2 block">
                                Name
                            </label>
                            <input type="text"
                            class="w-full bg-gray-800/50
                            border border-rose-500/30 rounded-xl px-4 py-3
                            text-white placeholder-rose-300
                            focus:border-rose-400 focus:outline-none transition-all ">
                        </div>
                        <div> 
                            <label type="email"
                            class="text-white text-sm 
                            font-medium mb-2 block">
                                Email
                            </label>
                            <input class="w-full bg-gray-800/50
                            border border-rose-500/30 rounded-xl px-4 py-3
                            text-white placeholder-rose-300
                            focus:border-rose-400 focus:outline-none transition-all ">
                        </div>
                    </div>
                        <div> 
                            <label type="text"
                            class="text-white text-sm 
                            font-medium mb-2 block">
                                Subject
                            </label>
                            <input class="w-full bg-gray-800/50
                            border border-rose-500/30 rounded-xl px-4 py-3
                            text-white placeholder-rose-300
                            focus:border-rose-400 focus:outline-none transition-all ">
                        </div>
                        <div> 
                            <label type="text"
                            class="text-white text-sm 
                            font-medium mb-2 block">
                                Subject
                            </label>
                            <textarea rows="4"
                             class="w-full bg-gray-800/50
                            border border-rose-500/30 rounded-xl px-4 py-3
                            text-white placeholder-rose-300
                            focus:border-rose-400 focus:outline-none transition-all "></textarea>
                        </div>
                        <button type="submit"
                            class="w-full bg-linear-to-r from-rose-500 to-pink-500 text-white font-semibold py-3 rounded-xl 
                            hover:shadow-lg hover:shadow-rose-500/25 transition-all
                            duration-300">
                            Send Message
                        </button>

                </form>

              </div>-->
        </div>
        </div>
        
    </section>
</template>

<script setup>
import { ChatBubbleLeftRightIcon, EnvelopeIcon, MapPinIcon, PhoneIcon, ShareIcon, UserGroupIcon } from '@heroicons/vue/16/solid';

</script>

<style>

</style>