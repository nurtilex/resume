<script setup>
import SideBar from "./components/SideBar.vue";
import NavBar from "./components/NavBar.vue";
import Introduce from "./sections/Introduce.vue";
import About from "./sections/About.vue";
import Experience from "./sections/Experience.vue";
import Skills from "./sections/Skills.vue";
import Contact from "./sections/Contact.vue";
import Mentoring from "./sections/Mentoring.vue";
import Recommendations from "./sections/Recommendations.vue";
</script>

<template>
  <main class="main">
    <SideBar />
    <div class="sections">
      <Introduce />
      <About />
      <Experience />
      <Mentoring />
      <Skills />
      <Recommendations />
      <Contact />
    </div>
  </main>
<NavBar />
</template>

<style scoped>
.main {
  position: relative;
  display: flex;
  flex-direction: row;
  gap: 2rem;
  min-height: 110vh;

  .sections {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    gap: 1rem;
    width: 100%;

    & > section {
      min-height: 100vh;
      scroll-behavior: smooth;
    }
  }
}
</style>
