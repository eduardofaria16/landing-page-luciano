<template>
  <section id="sobre" class="about">
    <div class="about__container">
      <div class="about__header">
        <h2 class="about__title">Conheça Nosso Diretor Presidente</h2>
        <p class="about__subtitle">
          Dedicado à promoção, autonomia e empoderamento das pessoas e organizações
        </p>
      </div>
      
      <div class="about__content">
        <div class="about__image">
          <div class="about__image-container">
            <img 
              src="/src/assets/_MG_2760.JPG" 
              alt="Luciano Tarso - Psicólogo Clínico e Organizacional"
              class="about__img"
            />
            <div class="about__badge">
              <span class="about__badge-text">25+ Anos</span>
              <span class="about__badge-subtitle">de Experiência</span>
            </div>
          </div>
        </div>
        
        <div class="about__text">
          <div class="about__intro">
            <h3 class="about__name">Luciano Tarso</h3>
            <p class="about__credentials">
              Palestrante, Psicólogo Clínico e Organizacional, Professor Universitário
            </p>
          </div>
          
          <div class="about__description">
            <p>
              Luciano Tarso é Palestrante, Psicólogo Clínico e Organizacional, Professor Universitário, de MBA e Pós Graduação. Durante sua trajetória profissional com mais de 25 anos de vivência, exerceu diversos cargos de liderança, sejam eles, no setor público e no privado, passando pelas áreas de supervisão, coordenação, gerência e direção de empresas, bem como de instituições de ensino.
            </p>
            
            <p>
              Além de possuir várias outras formações acadêmicas correlatas, como Administração e Mestrado em Educação, e 08 especializações, Luciano dedica seu tempo livre em aprofundar-se nas Artes e Teatro.
            </p>
            
            <p>
              Um estudioso da mente humana e suas correlações com os contextos que atravessam o sujeito (a pessoa) contemporâneo (a) por meio das relações de trabalho, sociais, íntimas, familiares e digitais, bem como um entusiasta do Humanismo, entende que o ser humano deve estar no centro de tudo aquilo que o cerca e que seu protagonismo e autonomia serão potencializados através de conexões profundas e saudáveis com seus pares.
            </p>
          </div>
          <div class="about__image-container">
            <img 
              src="/src/assets/rio.JPG" 
              alt="Luciano Tarso - Psicólogo Clínico e Organizacional"
              class="about__img"
            />
          </div>

          <div class="about__qualifications">
            <h4 class="about__qualifications-title">Formação e Especializações</h4>
            <div class="about__qualifications-grid">
              <div class="about__qualification">
                <span class="about__qualification-icon">🎓</span>
                <div class="about__qualification-text">
                  <strong>Psicologia</strong>
                  <span>Graduação</span>
                </div>
              </div>
              <div class="about__qualification">
                <span class="about__qualification-icon">📚</span>
                <div class="about__qualification-text">
                  <strong>Administração</strong>
                  <span>Graduação</span>
                </div>
              </div>
              <div class="about__qualification">
                <span class="about__qualification-icon">🎯</span>
                <div class="about__qualification-text">
                  <strong>Mestrado em Educação</strong>
                  <span>Pós-graduação</span>
                </div>
              </div>
              <div class="about__qualification">
                <span class="about__qualification-icon">⭐</span>
                <div class="about__qualification-text">
                  <strong>8 Especializações</strong>
                  <span>Áreas correlatas</span>
                </div>
              </div>
              <div class="about__qualification">
                <span class="about__qualification-icon">🎭</span>
                <div class="about__qualification-text">
                  <strong>Artes e Teatro</strong>
                  <span>Estudos complementares</span>
                </div>
              </div>
              <div class="about__qualification">
                <span class="about__qualification-icon">🏛️</span>
                <div class="about__qualification-text">
                  <strong>Professor Universitário</strong>
                  <span>MBA e Pós-graduação</span>
                </div>
              </div>
              <div class="about__qualification">
                <span class="about__qualification-icon">🎓</span>
                <div class="about__qualification-text">
                  <a href="http://lattes.cnpq.br/0000556466002008"><strong>Acesse Curriculo lattes</strong></a>
                </div>
              </div>
            </div>
          </div>
          
          <div class="about__philosophy">
            <h4 class="about__philosophy-title">Nossa Filosofia</h4>
            <div class="about__philosophy-content">
              <div class="about__philosophy-item">
                <span class="about__philosophy-icon">🤝</span>
                <div class="about__philosophy-text">
                  <strong>Humanismo</strong>
                  <p>O ser humano deve estar no centro de tudo aquilo que o cerca</p>
                </div>
              </div>
              <div class="about__philosophy-item">
                <span class="about__philosophy-icon">🌱</span>
                <div class="about__philosophy-text">
                  <strong>Protagonismo</strong>
                  <p>Potencializar a autonomia através de conexões profundas e saudáveis</p>
                </div>
              </div>
              <div class="about__philosophy-item">
                <span class="about__philosophy-icon">🔗</span>
                <div class="about__philosophy-text">
                  <strong>Conexões</strong>
                  <p>Relações de trabalho, sociais, íntimas, familiares e digitais</p>
                </div>
              </div>
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
.about {
  padding: var(--spacing-4xl) 0;
  background: var(--white);
}

.about__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--spacing-md);
}

.about__header {
  text-align: center;
  margin-bottom: var(--spacing-4xl);
}

.about__title {
  font-size: var(--font-size-4xl);
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: var(--spacing-md);
}

.about__subtitle {
  font-size: var(--font-size-lg);
  color: var(--text-light);
  max-width: 600px;
  margin: 0 auto;
}

.about__content {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: var(--spacing-4xl);
  align-items: start;
}

.about__image {
  position: relative;
}

.about__image-container {
  position: relative;
  border-radius: var(--border-radius-xl);
  overflow: hidden;
  box-shadow: var(--shadow-xl);
}

.about__img {
  width: 95%;
  height: 500px;
  object-fit: cover;
}

.about__badge {
  position: absolute;
  top: var(--spacing-xl);
  left: var(--spacing-xx);
  background: rgba(45, 74, 58, 0.9);
  backdrop-filter: blur(10px);
  padding: var(--spacing-lg);
  border-radius: var(--border-radius-lg);
  text-align: center;
  color: var(--white);
}

.about__badge-text {
  display: block;
  font-size: var(--font-size-2xl);
  font-weight: 700;
  color: var(--accent-color);
}

.about__badge-subtitle {
  display: block;
  font-size: var(--font-size-sm);
  margin-top: var(--spacing-xs);
}

.about__text {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-2xl);
}

.about__intro {
  padding-bottom: var(--spacing-xl);
  border-bottom: 2px solid var(--light-color);
}

.about__name {
  font-size: var(--font-size-3xl);
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: var(--spacing-sm);
}

.about__credentials {
  font-size: var(--font-size-lg);
  color: var(--accent-color);
  font-weight: 600;
}

.about__description {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.about__description p {
  font-size: var(--font-size-base);
  color: var(--text-light);
  line-height: 1.7;
  margin: 0;
}

.about__qualifications-title,
.about__philosophy-title {
  font-size: var(--font-size-xl);
  font-weight: 600;
  color: var(--primary-color);
  margin-bottom: var(--spacing-lg);
}

.about__qualifications-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--spacing-lg);
}

.about__qualification {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  padding: var(--spacing-lg);
  background: var(--light-color);
  border-radius: var(--border-radius-lg);
  transition: var(--transition-normal);
}

.about__qualification:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
}

.about__qualification-icon {
  font-size: var(--font-size-2xl);
  flex-shrink: 0;
}

.about__qualification-text {
  display: flex;
  flex-direction: column;
}

.about__qualification-text strong {
  font-size: var(--font-size-base);
  color: var(--primary-color);
  font-weight: 600;
}

.about__qualification-text span {
  font-size: var(--font-size-sm);
  color: var(--text-light);
}

.about__philosophy-content {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.about__philosophy-item {
  display: flex;
  gap: var(--spacing-lg);
  padding: var(--spacing-xl);
  background: linear-gradient(135deg, var(--light-color) 0%, #ffffff 100%);
  border-radius: var(--border-radius-lg);
  border-left: 4px solid var(--accent-color);
}

.about__philosophy-icon {
  font-size: var(--font-size-2xl);
  flex-shrink: 0;
}

.about__philosophy-text strong {
  display: block;
  font-size: var(--font-size-lg);
  color: var(--primary-color);
  font-weight: 600;
  margin-bottom: var(--spacing-xs);
}

.about__philosophy-text p {
  font-size: var(--font-size-base);
  color: var(--text-light);
  margin: 0;
  line-height: 1.6;
}

/* Responsividade */
@media (max-width: 1024px) {
  .about__content {
    gap: var(--spacing-3xl);
  }
  
  .about__img {
    height: 400px;
  }
  
  .about__qualifications-grid {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}

@media (max-width: 768px) {
  .about {
    padding: var(--spacing-3xl) 0;
  }
  
  .about__container {
    padding: 0 var(--spacing-sm);
  }
  
  .about__title {
    font-size: var(--font-size-3xl);
  }
  
  .about__content {
    grid-template-columns: 1fr;
    gap: var(--spacing-2xl);
  }
  
  .about__img {
    height: 300px;
  }
  
  .about__name {
    font-size: var(--font-size-2xl);
  }
  
  .about__credentials {
    font-size: var(--font-size-base);
  }
  
  .about__qualifications-grid {
    grid-template-columns: 1fr;
  }
  
  .about__philosophy-item {
    flex-direction: column;
    text-align: center;
    gap: var(--spacing-md);
  }
}

@media (max-width: 480px) {
  .about {
    padding: var(--spacing-2xl) 0;
  }
  
  .about__title {
    font-size: var(--font-size-2xl);
  }
  
  .about__subtitle {
    font-size: var(--font-size-base);
  }
  
  .about__text {
    gap: var(--spacing-xl);
  }
  
  .about__qualification {
    padding: var(--spacing-md);
  }
  
  .about__philosophy-item {
    padding: var(--spacing-lg);
  }
  
  .about__badge {
    top: var(--spacing-md);
    right: var(--spacing-md);
    padding: var(--spacing-md);
  }
  
  .about__badge-text {
    font-size: var(--font-size-xl);
  }
}
</style>
