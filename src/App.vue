<template>
  <NavBar/>
  <Presentation/>
  <SkillSection/>
  <ProjectsSection/>
  <ContactSection/>
  <router-view/>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Presentation from "@/components/Presentation.vue";
import SkillSection from "@/components/SkillSection.vue";
import ContactSection from "@/components/ContactSection.vue";
import ProjectsSection from './components/ProjectsSection.vue';

  export default {
    name: 'App',
    components: {
      NavBar,
      Presentation,
      SkillSection,
      ContactSection,
      ProjectsSection
    }
  }
</script>

<style>

</style>
