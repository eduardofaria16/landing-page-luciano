<template>
  <header class="header">
    <div class="header__container">
      <div class="header__brand">
        <div class="header__logo">
          <span class="header__logo-text">Instituto de Psicologia Aplicada</span>
        </div>
      </div>
      
      <nav class="header__nav" :class="{ 'header__nav--open': isMenuOpen }">
        <a href="#inicio" class="header__nav-link" @click="closeMenu">Início</a>
        <a href="#sobre" class="header__nav-link" @click="closeMenu">Sobre</a>
        <a href="#contato" class="header__nav-link" @click="closeMenu">Contato</a>
      </nav>
      
      <div class="header__actions">
        <a href="https://wa.me/message/JL5C2FM6USUGA1" class="header__cta">Agendar Consulta</a>
        <button 
          class="header__menu-toggle"
          @click="toggleMenu"
          :aria-expanded="isMenuOpen"
          aria-label="Menu de navegação"
        >
          <span class="header__menu-line"></span>
          <span class="header__menu-line"></span>
          <span class="header__menu-line"></span>
        </button>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}

const handleResize = () => {
  if (window.innerWidth > 768) {
    isMenuOpen.value = false
  }
}

onMounted(() => {
  window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
})
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: rgba(45, 74, 58, 0.95);
  backdrop-filter: blur(10px);
  z-index: 1000;
  padding: var(--spacing-sm) 0;
  transition: var(--transition-normal);
}

.header__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  align-items: center;
  gap: var(--spacing-lg);
}

.header__brand {
  grid-column: 2;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header__logo {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: var(--spacing-sm);
}

.header__logo-text {
  font-size: var(--font-size-xl);
  font-weight: 800;
  color: var(--accent-color);
  letter-spacing: 2px;
  text-align: center;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  white-space: nowrap;
}

.header__nav {
  grid-column: 1;
  justify-self: start;
}

.header__actions {
  grid-column: 3;
  justify-self: end;
}

.header__nav {
  display: flex;
  align-items: center;
  gap: var(--spacing-lg);
}

.header__nav-link {
  color: var(--white);
  text-decoration: none;
  font-weight: 500;
  font-size: var(--font-size-sm);
  padding: var(--spacing-sm) var(--spacing-md);
  border-radius: var(--border-radius-md);
  transition: var(--transition-fast);
  white-space: nowrap;
}

.header__nav-link:hover {
  background: rgba(212, 165, 116, 0.1);
  color: var(--accent-color);
}

.header__actions {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
}

.header__cta {
  background: var(--accent-color);
  color: var(--primary-color);
  text-decoration: none;
  padding: var(--spacing-sm) var(--spacing-lg);
  border-radius: var(--border-radius-md);
  font-weight: 600;
  font-size: var(--font-size-sm);
  transition: var(--transition-fast);
  white-space: nowrap;
}

.header__cta:hover {
  background: #E5B685;
  transform: translateY(-1px);
  box-shadow: var(--shadow-md);
}

.header__menu-toggle {
  display: none;
  flex-direction: column;
  gap: 4px;
  background: none;
  border: none;
  cursor: pointer;
  padding: var(--spacing-sm);
  border-radius: var(--border-radius-sm);
}

.header__menu-line {
  width: 24px;
  height: 2px;
  background: var(--white);
  transition: var(--transition-fast);
}

/* Responsividade */
@media (max-width: 1024px) {
  .header__logo-text {
    font-size: var(--font-size-lg);
    letter-spacing: 1.5px;
  }
}

@media (max-width: 768px) {
  .header__container {
    display: flex;
    justify-content: space-between;
    padding: 0 var(--spacing-sm);
  }
  
  .header__brand {
    flex: 1;
    justify-content: center;
    margin: 0 var(--spacing-md);
  }
  
  .header__logo-text {
    font-size: var(--font-size-base);
    letter-spacing: 1px;
  }
  
  .header__nav {
    position: fixed;
    top: 100%;
    left: 0;
    right: 0;
    background: var(--primary-color);
    flex-direction: column;
    padding: var(--spacing-xl);
    gap: var(--spacing-lg);
    transform: translateY(-100%);
    opacity: 0;
    visibility: hidden;
    transition: var(--transition-normal);
    box-shadow: var(--shadow-lg);
  }
  
  .header__nav--open {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }
  
  .header__nav-link {
    font-size: var(--font-size-base);
    padding: var(--spacing-md);
    text-align: center;
    border-bottom: 1px solid rgba(212, 165, 116, 0.1);
  }
  
  .header__cta {
    display: none;
  }
  
  .header__menu-toggle {
    display: flex;
  }
}

@media (max-width: 480px) {
  .header {
    padding: var(--spacing-xs) 0;
  }
  
  .header__logo-text {
    font-size: var(--font-size-sm);
    letter-spacing: 0.5px;
  }
  
  .header__container {
    gap: var(--spacing-xs);
  }
}

/* Efeito de destaque para o nome do instituto */
.header__logo-text {
  position: relative;
}

.header__logo-text::before {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 50%;
  transform: translateX(-50%);
  width: 60%;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent-color), transparent);
  opacity: 0.7;
}
</style>