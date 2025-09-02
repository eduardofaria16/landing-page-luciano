<template>
  <section id="inicio" class="hero">
    <div class="hero__container">
      <div class="hero__content">
        <!-- Imagem movida para dentro do grid -->
        <div class="hero__image">
          <div class="hero__image-container">
            <img 
              src="/src/assets/LOGOTIPO.png" 
              alt="Consultório de psicologia acolhedor e profissional"
              class="hero__img"
            />
          </div>
        </div>
        
        <!-- Conteúdo de texto -->
        <div class="hero__text">
          <h1 class="hero__title">
            Transformamos vidas, 
            <span class="hero__title-highlight">fortalecemos relações</span>
            e construímos ambientes mais saudáveis
          </h1>
          
          <p class="hero__subtitle">
            No Instituto de Psicologia Aplicada Luciano Tarso, acreditamos que o cuidado com a saúde emocional é a base para o crescimento pessoal e coletivo. Atuamos com dedicação, ciência e humanidade para ajudar pessoas e organizações a viverem com mais equilíbrio, propósito e qualidade de vida.
          </p>
          
          <div class="hero__actions">
            <a href="#contato" class="btn btn--primary">
              Dê o primeiro passo para o seu bem-estar
            </a>
            <a href="#sobre" class="btn btn--secondary">
              Conheça nossa abordagem
            </a>
          </div>
          
          <div class="hero__features">
            <div class="hero__feature">
              <span class="hero__feature-icon">🏥</span>
              <span class="hero__feature-text">Atendimento clínico especializado</span>
            </div>
            <div class="hero__feature">
              <span class="hero__feature-icon">🏢</span>
              <span class="hero__feature-text">Psicologia organizacional</span>
            </div>
            <div class="hero__feature">
              <span class="hero__feature-icon">🎓</span>
              <span class="hero__feature-text">Psicologia escolar</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  min-height: 100vh;
  background: linear-gradient(135deg, var(--light-color) 0%, #ffffff 100%);
  display: flex;
  align-items: center;
  padding: calc(var(--spacing-4xl) + 80px) 0 var(--spacing-3xl);
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 50%;
  height: 100%;
  background: linear-gradient(45deg, transparent 0%, rgba(45, 74, 58, 0.03) 100%);
  pointer-events: none;
}

.hero__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
  width: 100%;
}

.hero__content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--spacing-4xl);
  align-items: center;
}

.hero__image {
  /* Imagem fica na primeira coluna (esquerda) no desktop */
  grid-column: 1;
  grid-row: 1;
}

.hero__text {
  /* Texto fica na segunda coluna (direita) no desktop */
  grid-column: 2;
  grid-row: 1;
  max-width: 600px;
}

.hero__title {
  font-size: var(--font-size-5xl);
  font-weight: 700;
  color: var(--primary-color);
  line-height: 1.1;
  margin-bottom: var(--spacing-xl);
}

.hero__title-highlight {
  color: var(--accent-color);
  position: relative;
}

.hero__title-highlight::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 3px;
  background: linear-gradient(90deg, var(--accent-color), transparent);
  border-radius: 2px;
}

.hero__subtitle {
  font-size: var(--font-size-lg);
  color: var(--text-light);
  line-height: 1.6;
  margin-bottom: var(--spacing-2xl);
}

.hero__actions {
  display: flex;
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-3xl);
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: var(--spacing-lg) var(--spacing-2xl);
  border-radius: var(--border-radius-lg);
  text-decoration: none;
  font-weight: 600;
  font-size: var(--font-size-base);
  transition: var(--transition-normal);
  border: 2px solid transparent;
  cursor: pointer;
  white-space: nowrap;
}

.btn--primary {
  background: var(--accent-color);
  color: var(--primary-color);
  border-color: var(--accent-color);
}

.btn--primary:hover {
  background: #E5B685;
  border-color: #E5B685;
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

.btn--secondary {
  background: transparent;
  color: var(--primary-color);
  border-color: var(--primary-color);
}

.btn--secondary:hover {
  background: var(--primary-color);
  color: var(--white);
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

.hero__features {
  display: flex;
  gap: var(--spacing-xl);
}

.hero__feature {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
}

.hero__feature-icon {
  font-size: var(--font-size-xl);
}

.hero__feature-text {
  font-size: var(--font-size-sm);
  color: var(--text-light);
  font-weight: 500;
}

.hero__image-container {
  position: relative;
  border-radius: var(--border-radius-xl);
  overflow: hidden;
  box-shadow: var(--shadow-xl);
}

.hero__img {
  width: 100%;
  height: 600px;
  object-fit: cover;
  transition: var(--transition-slow);
}

.hero__image-overlay {
  position: absolute;
  right: var(--spacing-xl);
}

.hero__badge {
  background: rgba(45, 74, 58, 0.9);
  backdrop-filter: blur(10px);
  padding: var(--spacing-lg);
  border-radius: var(--border-radius-lg);
  text-align: center;
  color: var(--white);
}

.hero__badge-text {
  display: block;
  font-size: var(--font-size-2xl);
  font-weight: 700;
  color: var(--accent-color);
}

.hero__badge-subtitle {
  display: block;
  font-size: var(--font-size-sm);
  margin-top: var(--spacing-xs);
}

/* Responsividade */
@media (max-width: 1024px) {
  .hero__title {
    font-size: var(--font-size-4xl);
  }
  
  .hero__subtitle {
    font-size: var(--font-size-base);
  }
  
  .hero__content {
    gap: var(--spacing-3xl);
  }
  
  .hero__img {
    height: 400px;
  }
}

@media (max-width: 768px) {
  .hero {
    padding: calc(var(--spacing-3xl) + 80px) 0 var(--spacing-2xl);
    min-height: auto;
  }
  
  .hero__content {
    /* Muda para uma coluna no mobile */
    grid-template-columns: 1fr;
    gap: var(--spacing-2xl);
    text-align: center;
  }
  
  .hero__image {
    /* Imagem fica no topo no mobile */
    grid-column: 1;
    grid-row: 1;
    margin-bottom: var(--spacing-xl);
    width: 100%;
    max-width: 400px;
    justify-self: center;
  }
  
  .hero__text {
    /* Texto fica abaixo da imagem no mobile */
    grid-column: 1;
    grid-row: 2;
  }
  
  .hero__title {
    font-size: var(--font-size-3xl);
    margin-bottom: var(--spacing-lg);
  }
  
  .hero__subtitle {
    font-size: var(--font-size-base);
    margin-bottom: var(--spacing-xl);
  }
  
  .hero__actions {
    flex-direction: column;
    align-items: center;
    gap: var(--spacing-md);
  }
  
  .hero__features {
    justify-content: center;
    flex-wrap: wrap;
    gap: var(--spacing-lg);
  }
  
  .hero__img {
    height: 300px;
  }
  
  .hero__badge {
    padding: var(--spacing-md);
  }
  
  .hero__badge-text {
    font-size: var(--font-size-xl);
  }
}

@media (max-width: 480px) {
  .hero {
    padding: calc(var(--spacing-2xl) + 80px) 0;
  }
  
  .hero__container {
    padding: 0 var(--spacing-sm);
  }
  
  .hero__image {
    max-width: 300px;
    margin-bottom: var(--spacing-lg);
  }
  
  .hero__title {
    font-size: var(--font-size-2xl);
    line-height: 1.2;
  }
  
  .hero__subtitle {
    font-size: var(--font-size-sm);
    line-height: 1.5;
  }
  
  .btn {
    padding: var(--spacing-md) var(--spacing-lg);
    font-size: var(--font-size-sm);
    width: 100%;
    max-width: 280px;
  }
  
  .hero__features {
    flex-direction: column;
    gap: var(--spacing-md);
  }
  
  .hero__feature {
    justify-content: center;
  }
  
  .hero__img {
    height: 350px;
  }
  
  .hero__image-overlay {
    right: var(--spacing-md);
  }
  
  .hero__content {
    gap: var(--spacing-xl);
  }
}

@media (max-width: 360px) {
  .hero {
    padding: calc(var(--spacing-xl) + 80px) 0;
  }
  
  .hero__image {
    max-width: 250px;
    margin-bottom: var(--spacing-md);
  }
  
  .hero__title {
    font-size: var(--font-size-xl);
  }
  
  .hero__subtitle {
    font-size: var(--font-size-xs);
  }
  
  .btn {
    padding: var(--spacing-sm) var(--spacing-md);
    font-size: var(--font-size-xs);
  }
  
  .hero__img {
    height: 200px;
  }
}
</style>