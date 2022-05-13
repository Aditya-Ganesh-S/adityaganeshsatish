<template>
  <div>
    <Header />
    <About />
    <Skills />
    <Experience />
    <Projects />
    <Feedback />
    <Contact />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Experience from './components/Experiences.vue'
import Projects from './components/Projects.vue';
import Feedback from './components/Feedback.vue';
import Contact from './components/Contact.vue';
export default {
  name: 'App',
  components: {
    Header,
    About,
    Skills,
    Experience,
    Projects,
    Feedback,
    Contact
  }
}
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
* {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      font-weight: 400;
      font-size: 14px;
      color: #777;
      font-family: 'Playfair Display', serif;
      @include respond(tab-land){
        font-size: 12px;
      }
      @include respond(tab-port){
        font-size: 10px;
      }

      @include respond(phone){
        font-size: 8px;
      }
      
      @include respond(big-desktop){
        font-size: 18px;
      }
    }

    body{
      padding: 3rem;
      
      @include respond(tab-port){
        padding: 0rem;
      }
    }
</style> 
