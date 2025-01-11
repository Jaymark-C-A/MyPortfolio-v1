<template>
  <Header />
  <HeroSection />
  <AboutSection />
  <Stack />
  <ProjectsSection />
  <ContactSection />
  <Footer />
</template>

<script lang="ts">
import Header from "./components/Header.vue";
import HeroSection from "./components/HeroSection.vue";
import AboutSection from "./components/AboutSection.vue";
import Stack from "./components/Stack.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import ContactSection from "./components/ContactSection.vue";
import Footer from "./components/Footer.vue";


export default {
  name: "App",
  components: {
    Header,
    HeroSection,
    AboutSection,
    Stack,
    ProjectsSection,
    ContactSection,
    Footer,
  },
};
</script>

<style>
  html, body {
    overflow-x: hidden;
    background: #cecece;
  }
  .fade-right {
    opacity: 0;
    transform: translateX(-50px);
    transition: opacity 0.5s ease-out, transform 0.5s ease-out;
  }

  .fade-right.visible {
    opacity: 1;
    transform: translateX(0);
  }

  .fade-left {
    opacity: 0;
    transform: translateX(50px); /* Offset to the right */
    transition: opacity 0.5s ease-out, transform 0.5s ease-out;
  }

  .fade-left.visible {
    opacity: 1;
    transform: translateX(0); /* Bring to original position */
  }

</style>
