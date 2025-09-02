<script setup>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Approach from './components/Approach.vue'
import Testimonials from './components/Testimonials.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div id="app">
    <Header />
    <main>
      <Hero />
      <About />
      <Services />
      <Approach />
      <Testimonials />
      <Contact />
    </main>
    <Footer />
  </div>
</template>

<style>
/* Importando a fonte Baradig */
@font-face {
  font-family: 'Baradig';
  src: url('/fonts/Baradig-Regular.woff2') format('woff2'),
       url('/fonts/Baradig-Regular.woff') format('woff');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Baradig';
  src: url('/fonts/Baradig-Bold.woff2') format('woff2'),
       url('/fonts/Baradig-Bold.woff') format('woff');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

/* Reset e estilos globais */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Baradig', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  line-height: 1.6;
  color: var(--text-dark);
  overflow-x: hidden;
  background-color: var(--white);
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1;
}

/* Utilitários específicos do App */
.text-gradient {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.bg-gradient {
  background: linear-gradient(135deg, var(--light-color) 0%, var(--white) 100%);
}

/* Responsividade específica do App */
@media (max-width: 768px) {
  #app {
    min-height: auto;
  }
}

@media (max-width: 480px) {
  body {
    font-size: var(--font-size-sm);
  }
}
</style>
