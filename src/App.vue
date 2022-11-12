<template>
  <div id="app">
    <Navbar />
    <Hero />
    <About />
    <Value />
  </div>
</template>

<script>
import Navbar from './components/NavbarHeader.vue'
import Hero from './components/HeroPage.vue'
import About from './components/AboutPage.vue'
import Value from './components/ValuePage.vue'


export default {
  components: {
    'Navbar': Navbar,
    'Hero': Hero,
    'About': About,
    'Value': Value,

  },
  data() {
    return {
      
    }
  }
}
</script>

<style scoped>

</style>
