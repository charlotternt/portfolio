<template>
  <div class="app-container">
    <Navbar class="navbar margin-container" />
    <main class="content margin-container">
      <section id="home"><Home /></section>
      <section id="about"><About /></section>
      <section id="stack"><Stack /></section>
      <section id="projects"><Project /></section>
      <section id="experience"><Experience /></section>
      <section id="social"><Social /></section>
    </main>
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/navbar.vue";
import Home from "./components/home.vue";
import About from "./components/about.vue";
import Project from "./components/project.vue";
import Experience from "./components/experience.vue";
import Footer from "./components/footer.vue";
import Stack from "./components/stack.vue";
import Social from "./components/social.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    About,
    Stack,
    Project,
    Experience,
    Footer,
    Social,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Dosis:wght@200..800&display=swap");

body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  font-family: "Dosis", sans-serif;
  display: flex;
  flex-direction: column;
}

html {
  scroll-behavior: smooth;
}

html,
body,
#app {
  height: 100%;
}

h1 {
  color: #6540ca;
  margin-bottom: 5px;
  font-size: 44px;
}

h2 {
  margin-top: 0;
  margin-bottom: 5px;
}

h3 {
  margin-top: 0;
  margin-bottom: 5px;
}

h2,
h3 {
  color: #c9b8f5;
  font-size: 38px;
}

p {
  font-size: 20px;
}

.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.content {
  flex: 1;
}

.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}
</style>
