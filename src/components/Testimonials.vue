<template>
  <section class="testimonials section">
    <div class="container">
      <h2 class="section-title">O Que Dizem os Meus Pacientes</h2>
      <p class="section-subtitle">
        Testemunhos reais de pessoas que encontraram o seu caminho para o bem-estar emocional
      </p>
      
      <div class="testimonials__grid">
        <div class="testimonial-card" v-for="testimonial in testimonials" :key="testimonial.id">
          <div class="testimonial-card__content">
            <div class="testimonial-card__quote">
              <span class="testimonial-card__quote-mark">"</span>
              <p class="testimonial-card__text">{{ testimonial.text }}</p>
            </div>
            <div class="testimonial-card__author">
              <div class="testimonial-card__avatar">
                {{ testimonial.initials }}
              </div>
              <div class="testimonial-card__info">
                <h4 class="testimonial-card__name">{{ testimonial.name }}</h4>
                <span class="testimonial-card__service">{{ testimonial.service }}</span>
              </div>
            </div>
          </div>
          <div class="testimonial-card__rating">
            <div class="stars">
              <span v-for="n in 5" :key="n" class="star">★</span>
            </div>
          </div>
        </div>
      </div>
      
      <div class="testimonials__stats">
      
        <div class="stat-item">
          <div class="stat-item__number">Instituto De Psicologia Aplicada</div>
        </div>
        <div class="stat-item">
          <div class="stat-item__number">Luciano Tarso</div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    id: 1,
    text: 'Cheguei aos 40 anos e muito angustiado com minha situação profissional...precisava mudar...não estava legal. Procurei o Dr. Luciano e foi como um bálsamo! Ele me ajudou bastante fazer minha transição de carreira e hoje estou muito satisfeito com minha nova vida.',
    name: 'Maria S, 40 anos',
    initials: 'MS',
    service: 'Terapia Individual'
  },
  {
    id: 2,
    text: 'Meu filho estava enfrentando dificuldades de aprendizagem e baixa autoestima na escola. Com o acompanhamento do Dr. Luciano, ele desenvolveu estratégias para melhorar o foco e a confiança. Hoje é uma criança muito mais feliz e motivada.',
    name: 'Ana P, 47 anos',
    initials: 'AP',
    service: 'Psicologia Escolar'
  },
  {
    id: 3,
    text: 'Sofria de ansiedade há anos e não conseguia encontrar uma solução. Com as técnicas terapêuticas e o acompanhamento do Dr. Luciano, aprendi a gerir minha ansiedade de forma eficaz. Muito obrigada pela transformação!',
    name: 'Carla M, 23 anos',
    initials: 'CM',
    service: 'Terapia Clínica'
  },
  {
    id: 4,
    text: 'Nossa escola estava passando por um momento muito difícil...pais, alunos e professores não conseguiam alinhar suas expectativas para com o outro. O Dr. Luciano foi fundamental no processo de organização sistêmica da nossa Comunidade Escolar. Estamos muito felizes com o resultado',
    name: 'Diretora Regina, 53 anos',
    initials: 'PR',
    service: 'Psicologia Escolar'
  },
  {
    id: 5,
    text: 'A terapia individual me ajudou a resolver traumas antigos e a desenvolver uma autoestima mais saudável. O ambiente seguro e acolhedor criado pelo Dr. Luciano permitiu que eu me expressasse livremente e encontrasse meu equilíbrio emocional.',
    name: 'Carlos Silva',
    initials: 'CS',
    service: 'Terapia Individual'
  },
  {
    id: 6,
    text: 'Profissional excepcional! O Psicologo Luciano tem uma capacidade única de nos fazer sentir compreendidos e apoiados. Suas técnicas são eficazes e os resultados são visíveis desde as primeiras sessões. Recomendo sem hesitar!',
    name: 'Ricardo T.',
    initials: 'RT',
    service: 'Terapia Clínica'
  }
]
</script>

<style scoped>
.testimonials {
  background-color: var(--white);
}

.testimonials__grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-2xl);
}

.testimonial-card {
  background-color: var(--light-gray);
  border-radius: 16px;
  padding: var(--spacing-xl);
  position: relative;
  transition: all var(--transition-normal);
  border: 1px solid rgba(48, 56, 41, 0.1);
}

.testimonial-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
  border-color: var(--accent-color);
}

.testimonial-card__content {
  margin-bottom: var(--spacing-md);
}

.testimonial-card__quote {
  position: relative;
  margin-bottom: var(--spacing-lg);
}

.testimonial-card__quote-mark {
  position: absolute;
  top: -10px;
  left: -10px;
  font-size: 4rem;
  color: var(--accent-color);
  opacity: 0.3;
  font-family: serif;
  line-height: 1;
}

.testimonial-card__text {
  color: var(--neutral-color);
  line-height: 1.6;
  font-style: italic;
  margin: 0;
  padding-left: var(--spacing-md);
}

.testimonial-card__author {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
}

.testimonial-card__avatar {
  width: 50px;
  height: 50px;
  background-color: var(--accent-color);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  font-size: var(--font-size-base);
  flex-shrink: 0;
}

.testimonial-card__info {
  flex: 1;
}

.testimonial-card__name {
  font-size: var(--font-size-base);
  font-weight: 600;
  color: var(--primary-color);
  margin: 0 0 var(--spacing-xs) 0;
}

.testimonial-card__service {
  font-size: var(--font-size-small);
  color: var(--accent-color);
  font-weight: 500;
}

.testimonial-card__rating {
  display: flex;
  justify-content: center;
  margin-top: var(--spacing-md);
  padding-top: var(--spacing-md);
  border-top: 1px solid rgba(48, 56, 41, 0.1);
}

.stars {
  display: flex;
  gap: 2px;
}

.star {
  color: #ffd700;
  font-size: var(--font-size-large);
}

.testimonials__stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: var(--spacing-lg);
  padding: var(--spacing-2xl);
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  border-radius: 16px;
  color: white;
}

.stat-item {
  text-align: center;
}

.stat-item__number {
  font-size: var(--font-size-3xl);
  font-weight: 700;
  margin-bottom: var(--spacing-xs);
  color: white;
}

.stat-item__label {
  font-size: var(--font-size-base);
  opacity: 0.9;
  font-weight: 500;
}

/* Animação dos números */
@keyframes countUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.stat-item__number {
  animation: countUp 0.8s ease-out;
}

/* Responsividade */
@media (max-width: 768px) {
  .testimonials__grid {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
  
  .testimonial-card {
    padding: var(--spacing-lg);
  }
  
  .testimonials__stats {
    grid-template-columns: repeat(2, 1fr);
    gap: var(--spacing-md);
    padding: var(--spacing-lg);
  }
}

@media (max-width: 480px) {
  .testimonials__grid {
    grid-template-columns: 1fr;
  }
  
  .testimonial-card {
    min-width: auto;
  }
  
  .testimonials__stats {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .stat-item__number {
    font-size: var(--font-size-2xl);
  }
  
  .testimonial-card__quote-mark {
    font-size: 3rem;
  }
}
</style>

