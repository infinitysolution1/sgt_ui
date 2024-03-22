<script setup>
import Home from './components/Home.vue'
import AppFooter from './components/AppFooter.vue'
import Services from './components/Services.vue'
import Navbar from './components/Navbar.vue'
import ContactUs from './components/ContactUs.vue'
import About from './components/About.vue'
import OurFleet from './components/OurFleet.vue'
import FAQ from './components/FAQ.vue'
import Testimonials from './components/Testimonials.vue'
</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <section id="home">
      <Home />
    </section>
    <section id="services">
      <Services />
    </section>
    <section id="ourfleet">
      <OurFleet />
    </section>
    <section id="about">
      <About />
    </section>
    <section id="testimonials">
      <Testimonials />
    </section>
    <section id="about">
      <FAQ />
    </section>
    <section id="contactUs">
      <ContactUs />
    </section>
    <footer>
      <AppFooter />
    </footer>
  </main>

</template>

<style scoped>
header {
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
}

footer {
  width: 100vw;
  bottom: 0;
  left: 0;
  z-index: 100;
}

section {
  flex: 1;
  display: flex;
  min-height: 100vh;
  width: 100vw;
  overflow-y: hidden;
}

main {
  width: 100vw;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  left: 0;
  top: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }


  header .wrapper {
    display: flex;
  }
}
</style>
