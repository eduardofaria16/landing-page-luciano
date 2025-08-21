<template>
  <footer class="footer section ">
    <div class="footer__content">
      <div class="footer__brand">
        <h3 class="footer__logo">Dr. Ana Silva</h3>
        <p class="footer__tagline">Psicóloga Clínica</p>
        <p class="footer__description">
          Dedicada ao seu bem-estar mental e emocional. 
          Juntos, encontraremos o caminho para uma vida mais plena e equilibrada.
        </p>
        <div class="footer__social">
          <a href="#" class="footer__social-link" aria-label="LinkedIn">
            <span class="footer__social-icon">💼</span>
          </a>
          <a href="#" class="footer__social-link" aria-label="Instagram">
            <span class="footer__social-icon">📷</span>
          </a>
          <a href="#" class="footer__social-link" aria-label="Facebook">
            <span class="footer__social-icon">📘</span>
          </a>
        </div>
      </div>
      
      <div class="footer__links">
        <div class="footer__column">
          <h4 class="footer__column-title">Serviços</h4>
          <ul class="footer__list">
            <li><a href="#servicos" class="footer__link">Terapia Individual</a></li>
            <li><a href="#servicos" class="footer__link">Terapia de Casal</a></li>
            <li><a href="#servicos" class="footer__link">Terapia Familiar</a></li>
            <li><a href="#servicos" class="footer__link">Gestão do Stress</a></li>
            <li><a href="#servicos" class="footer__link">Orientação Vocacional</a></li>
          </ul>
        </div>
        
        <div class="footer__column">
          <h4 class="footer__column-title">Informações</h4>
          <ul class="footer__list">
            <li><a href="#sobre" class="footer__link">Sobre Mim</a></li>
            <li><a href="#abordagem" class="footer__link">Abordagem</a></li>
            <li><a href="#" class="footer__link">Política de Privacidade</a></li>
            <li><a href="#" class="footer__link">Termos de Serviço</a></li>
            <li><a href="#" class="footer__link">FAQ</a></li>
          </ul>
        </div>
        
        <div class="footer__column">
          <h4 class="footer__column-title">Contacto</h4>
          <div class="footer__contact">
            <div class="footer__contact-item">
              <span class="footer__contact-icon">📍</span>
              <span>Rua das Flores, 123<br>1200-123 Lisboa</span>
            </div>
            <div class="footer__contact-item">
              <span class="footer__contact-icon">📞</span>
              <span>+351 912 345 678</span>
            </div>
            <div class="footer__contact-item">
              <span class="footer__contact-icon">✉️</span>
              <span>ana.silva@psicologa.pt</span>
            </div>
          </div>
        </div>
        
        <div class="footer__column">
          <h4 class="footer__column-title">Horários</h4>
          <div class="footer__schedule">
            <div class="footer__schedule-item">
              <span class="footer__schedule-day">Segunda - Sexta</span>
              <span class="footer__schedule-time">9h00 - 19h00</span>
            </div>
            <div class="footer__schedule-item">
              <span class="footer__schedule-day">Sábado</span>
              <span class="footer__schedule-time">9h00 - 13h00</span>
            </div>
            <div class="footer__schedule-item">
              <span class="footer__schedule-day">Domingo</span>
              <span class="footer__schedule-time">Fechado</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <div class="footer__bottom">
      <div class="footer__bottom-content">
        <div class="footer__copyright">
          <p>&copy; {{ currentYear }} Dra. Ana Silva - Psicóloga Clínica. Todos os direitos reservados.</p>
        </div>
        <div class="footer__credentials">
          <span class="footer__credential">CRP 06/123456</span>
          <span class="footer__credential">Ordem dos Psicólogos Portugueses</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.footer {
  background: linear-gradient(135deg, var(--primary-color) 0%, #2a3021 100%);
  color: white;
  .footer {
  /* ... */
  padding: var(--spacing-4xl) 0 var(--spacing-lg); /* Antes tinha padding lateral */
}
}

.footer__content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
  display: grid;
  grid-template-columns: 1.5fr 2fr;
  gap: var(--spacing-2xl);
  margin-bottom: var(--spacing-2xl);
  padding: 0 var(--spacing-md); /* Adicionado padding lateral aqui */
  max-width: 1200px;
}

.footer__brand {
  max-width: 400px;
}

.footer__logo {
  font-size: var(--font-size-2xl);
  font-weight: 700;
  color: white;
  margin: 0 0 var(--spacing-xs) 0;
}

.footer__tagline {
  color: var(--accent-color);
  font-size: var(--font-size-base);
  font-weight: 600;
  margin: 0 0 var(--spacing-md) 0;
}

.footer__description {
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.6;
  margin-bottom: var(--spacing-lg);
}

.footer__social {
  display: flex;
  gap: var(--spacing-sm);
}

.footer__social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  transition: all var(--transition-normal);
  text-decoration: none;
}

.footer__social-link:hover {
  background-color: var(--accent-color);
  transform: translateY(-2px);
}

.footer__social-icon {
  font-size: var(--font-size-large);
}

.footer__links {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--spacing-xl);
}

.footer__column-title {
  font-size: var(--font-size-large);
  font-weight: 600;
  color: white;
  margin: 0 0 var(--spacing-md) 0;
  position: relative;
}

.footer__column-title::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 0;
  width: 30px;
  height: 2px;
  background-color: var(--accent-color);
}

.footer__list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer__list li {
  margin-bottom: var(--spacing-xs);
}

.footer__link {
  color: rgba(255, 255, 255, 0.8);
  text-decoration: none;
  font-size: var(--font-size-small);
  transition: color var(--transition-fast);
}

.footer__link:hover {
  color: var(--accent-color);
}

.footer__contact {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-sm);
}

.footer__contact-item {
  display: flex;
  align-items: flex-start;
  gap: var(--spacing-sm);
  color: rgba(255, 255, 255, 0.8);
  font-size: var(--font-size-small);
}

.footer__contact-icon {
  font-size: var(--font-size-base);
  flex-shrink: 0;
}

.footer__schedule {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.footer__schedule-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: rgba(255, 255, 255, 0.8);
  font-size: var(--font-size-small);
}

.footer__schedule-day {
  font-weight: 500;
}

.footer__schedule-time {
  color: var(--accent-color);
}

.footer__bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding: var(--spacing-lg) 0;
  width: 100%;
}

.footer__bottom-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: var(--spacing-md);
  padding: 0 var(--spacing-md); /* Adicionado padding lateral aqui */
  max-width: 1200px; /* Mantém o conteúdo centralizado */
}

.footer__copyright p {
  color: rgba(255, 255, 255, 0.6);
  font-size: var(--font-size-small);
  margin: 0;
}

.footer__credentials {
  display: flex;
  gap: var(--spacing-md);
  flex-wrap: wrap;
}

.footer__credential {
  color: rgba(255, 255, 255, 0.6);
  font-size: var(--font-size-small);
  padding: var(--spacing-xs) var(--spacing-sm);
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 4px;
}

/* Responsividade */
@media (max-width: 1024px) {
  .footer__content {
    grid-template-columns: 1fr;
    gap: var(--spacing-xl);
  }
  
  .footer__links {
    grid-template-columns: repeat(2, 1fr);
    gap: var(--spacing-lg);
  }
}

@media (max-width: 768px) {
  .footer__links {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
  
  .footer__bottom-content {
    flex-direction: column;
    text-align: center;
  }
  
  .footer__credentials {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .footer {
    padding: var(--spacing-xl) 0 0;
  }
  
  .footer__logo {
    font-size: var(--font-size-xl);
  }
  
  .footer__social {
    justify-content: center;
  }
  
  .footer__contact-item,
  .footer__schedule-item {
    flex-direction: column;
    align-items: flex-start;
    gap: var(--spacing-xs);
  }
}
</style>