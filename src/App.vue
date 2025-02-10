<script setup>
import HeroSection from "./components/HeroSection.vue";
import AboutMe from "./components/AboutMe.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
</script>

<template>
  <div class="portfolio">

    <main>
      <Header />
      <HeroSection />
      <AboutMe />
      <Skills />
      <Projects />
      <Contact />
    </main>

    <Footer />
  </div>
</template>

<style>
:root {
  --primary-color: #00ffdd;
  --bg-color: #1a1e23;
  --text-color: #ffffff;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
  font-family: Arial, sans-serif;
}

.portfolio {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.navigation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 0;
}

.nav-brand {
  font-size: 1.5rem;
  color: var(--primary-color);
}

.nav-links a {
  color: var(--text-color);
  text-decoration: none;
  margin-left: 2rem;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: var(--primary-color);
}

main {
  padding: 2rem 0;
}
</style>
