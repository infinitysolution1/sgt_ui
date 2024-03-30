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

  <div class="contactnow">
    <h2>Contact us on </h2>
    <p>+91 7976711820</p>
    <p>+91 9829285925</p>
  </div>

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

.contactnow {
  position: fixed;
  bottom: 0;
  right: 0;
  padding: 8px 16px;
  margin: 1.5%;
  background-color: #451d03;
  color: white;
  font-size: 0.75rem;
  border-radius: 4px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index: 100;
}

.contactnow h2 {
  font-size: 0.75rem;
  margin: 0;
}

.contactnow p {
  font-size: 1rem;
  margin: 0;
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
