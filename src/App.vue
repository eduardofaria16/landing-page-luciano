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

:root {
  /* Cores */
  --primary-color: #303829;
  --accent-color: #D18552;
  --secondary-color: #91907E;
  --light-color: #F5F1E8;
  --white: #ffffff;
  --dark-gray: #2c3e50;
  --text-light: #6B7280;

  /* Tipografia */
  --font-family: 'Baradig', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-size-xs: 12px;
  --font-size-sm: 14px;
  --font-size-base: 16px;
  --font-size-lg: 18px;
  --font-size-xl: 20px;
  --font-size-2xl: 24px;
  --font-size-3xl: 32px;
  --font-size-4xl: 40px;
  --font-size-5xl: 48px;

  /* Espaçamentos */
  --spacing-xs: 0.25rem;
  --spacing-sm: 0.5rem;
  --spacing-md: 1rem;
  --spacing-lg: 1.5rem;
  --spacing-xl: 2rem;
  --spacing-2xl: 3rem;
  --spacing-3xl: 4rem;
  --spacing-4xl: 5rem;

  /* Sombras */
  --shadow-sm: 0 1px 2px 0 rgba(45, 74, 58, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(45, 74, 58, 0.1);
  --shadow-lg: 0 10px 15px -3px rgba(45, 74, 58, 0.1);
  --shadow-xl: 0 20px 25px -5px rgba(45, 74, 58, 0.1);

  /* Transições */
  --transition-fast: 0.15s ease-in-out;
  --transition-normal: 0.3s ease-in-out;
  --transition-slow: 0.5s ease-in-out;

  /* Bordas */
  --border-radius-sm: 4px;
  --border-radius-md: 8px;
  --border-radius-lg: 12px;
  --border-radius-xl: 16px;
}

html {
  scroll-behavior: smooth;
  font-family: var(--font-family);
}

body {
  font-family: var(--font-family);
  font-size: var(--font-size-base);
  line-height: 1.6;
  color: var(--primary-color);
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

/* Utilitários */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
}

.section {
  padding: var(--spacing-2xl) 0;
}

.section-title {
  font-family: var(--font-family);
  font-size: var(--font-size-2xl);
  font-weight: 700;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: var(--spacing-xl);
}

.section-subtitle {
  font-family: var(--font-family);
  font-size: var(--font-size-lg);
  color: var(--secondary-color);
  text-align: center;
  margin-bottom: var(--spacing-lg);
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.btn {
  display: inline-block;
  padding: var(--spacing-sm) var(--spacing-lg);
  border: none;
  border-radius: var(--border-radius-md);
  font-family: var(--font-family);
  font-size: var(--font-size-base);
  font-weight: 600;
  text-decoration: none;
  text-align: center;
  cursor: pointer;
  transition: all var(--transition-normal);
}

.btn-primary {
  background-color: var(--accent-color);
  color: var(--white);
}

.btn-primary:hover {
  background-color: #b8713d;
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

.btn-secondary {
  background-color: transparent;
  color: var(--primary-color);
  border: 2px solid var(--primary-color);
}

.btn-secondary:hover {
  background-color: var(--primary-color);
  color: var(--white);
}

/* Responsividade */
@media (max-width: 768px) {
  .container {
    padding: 0 var(--spacing-sm);
  }
  
  .section {
    padding: var(--spacing-xl) 0;
  }
  
  .section-title {
    font-size: var(--font-size-xl);
  }
  
  .section-subtitle {
    font-size: var(--font-size-base);
  }
}


</style>
