<template>
  <div id="app">
    <Navbar />
    <Header />
    <About />
    <Skills />
    <Projects />
    <Contact />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Header from './components/Header.vue'
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    About,
    Skills,
    Projects,
    Contact
  }
}
</script>

<style>
:root {
  --primary: #2c3e50;
  --secondary: #42b983;
  --accent: #ffc107;
  --light: #f8f9fa;
  --dark: #343a40;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
}

section {
  padding: 4rem 2rem;
  min-height: 100vh;
}
</style>