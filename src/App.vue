<template>
  <NavBar/>
  <Presentation/>
  <SkillSection/>
  <router-view/>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Presentation from "@/components/Presentation.vue";
import SkillSection from "@/components/SkillSection.vue";

  export default {
    name: 'App',
    components: {
      NavBar,
      Presentation,
      SkillSection,
    }
  }
</script>

<style>

</style>
