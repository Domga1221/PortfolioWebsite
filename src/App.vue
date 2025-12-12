
<template>
  <div class="min-h-screen 
  bg-linear-to-br from-gray-900 
  via-rose-900 to-gray-900">
    <Navbar />
    <Hero />
    <Services />
    <About />
    <ExperienceSkills />
    <Projects />
    <Contact />
    <Footer />

    <BackToTop/>
  </div>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'


import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Services from './components/Services.vue'
import About from './components/About.vue'

import { ref, nextTick, onMounted } from 'vue'
import ExperienceSkills from './components/ExperienceSkills.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
import BackToTop from './components/BackToTop.vue'

export default {
  components: {
    Navbar,
    Hero,
    Services,
    About,
    ExperienceSkills,
    Projects,
    Contact,
    Footer,
    BackToTop
  },
  setup() {
    const loading = ref(true);
    onMounted(async() => {
      AOS.init({
        duration: 800,
        once: false,
        offset: 100,
        easing: 'ease-in-out'
      })
      setTimeout(()=>{
        loading.value = false;
      }, 800);
      return {loading};
    });
  }
}
</script>

<style scoped>

</style>
