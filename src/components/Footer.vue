<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__content">
        <div class="footer__main">
          <h3 class="footer__name">Luciano Tarso</h3>
          <p class="footer__credentials">Psicólogo Clínico - CRP-04 / 82152</p>
          <p class="footer__location">Uberlândia, MG</p>
        </div>
        
        <div class="footer__contact">
          <p class="footer__email">tarsoluciano@gmail.com</p>
          <p class="footer__phone">(34) 99687-7462</p>
        </div>
      </div>
      
      <div class="footer__bottom">
        <p class="footer__copyright">
          &copy; {{ currentYear }} Luciano Tarso - Todos os direitos reservados.
        </p>
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
  background-color: #303829;
  color: #fff;
  padding: var(--spacing-2xl) 0 var(--spacing-lg);
}

.footer__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
}

.footer__content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--spacing-xl);
  gap: var(--spacing-xl);
}

.footer__main {
  flex: 1;
}

.footer__name {
  font-size: var(--font-size-xl);
  font-weight: 700;
  margin-bottom: var(--spacing-sm);
  color: #fff;
}

.footer__credentials {
  font-size: var(--font-size-base);
  margin-bottom: var(--spacing-xs);
  color: #e0e0e0;
}

.footer__location {
  font-size: var(--font-size-base);
  color: #e0e0e0;
}

.footer__contact {
  text-align: right;
}

.footer__email {
  font-size: var(--font-size-base);
  margin-bottom: var(--spacing-xs);
  color: #e0e0e0;
}

.footer__phone {
  font-size: var(--font-size-base);
  color: #e0e0e0;
}

.footer__bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding-top: var(--spacing-lg);
  text-align: center;
}

.footer__copyright {
  font-size: var(--font-size-sm);
  color: #ccc;
  margin: 0;
}

/* Responsividade */
@media (max-width: 768px) {
  .footer {
    padding: var(--spacing-xl) 0 var(--spacing-md);
  }
  
  .footer__container {
    padding: 0 var(--spacing-sm);
  }
  
  .footer__content {
    /* Mantém lado a lado no mobile */
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    gap: var(--spacing-md);
  }
  
  .footer__main {
    flex: 1;
    text-align: left;
  }
  
  .footer__contact {
    flex: 1;
    text-align: right;
  }
  
  .footer__name {
    font-size: var(--font-size-lg);
  }
  
  .footer__credentials,
  .footer__location,
  .footer__email,
  .footer__phone {
    font-size: var(--font-size-sm);
  }
}

@media (max-width: 480px) {
  .footer {
    padding: var(--spacing-lg) 0 var(--spacing-md);
  }
  
  .footer__content {
    /* Continua lado a lado mesmo em telas muito pequenas */
    flex-direction: row;
    gap: var(--spacing-sm);
  }
  
  .footer__name {
    font-size: var(--font-size-base);
  }
  
  .footer__credentials,
  .footer__location,
  .footer__email,
  .footer__phone {
    font-size: var(--font-size-xs);
  }
  
  .footer__copyright {
    font-size: var(--font-size-xs);
  }
}

/* Para telas muito pequenas onde pode ficar apertado */
@media (max-width: 360px) {
  .footer__content {
    gap: var(--spacing-xs);
  }
  
  .footer__name,
  .footer__credentials,
  .footer__location,
  .footer__email,
  .footer__phone {
    font-size: var(--font-size-xs);
  }
  
  .footer__name {
    margin-bottom: var(--spacing-xs);
  }
  
  .footer__credentials {
    margin-bottom: var(--spacing-xs);
  }
  
  .footer__email {
    margin-bottom: var(--spacing-xs);
  }
}
</style>