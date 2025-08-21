<template>
  <section id="servicos" class="services section">
    <div class="container">
      <h2 class="section-title">Serviços</h2>
      <p class="section-subtitle">
        Ofereço acompanhamento psicológico especializado para diferentes necessidades e faixas etárias
      </p>
      
      <div class="services__grid">
        <div class="service-card" v-for="service in services" :key="service.id">
          <div class="service-card__icon">
            {{ service.icon }}
          </div>
          <h3 class="service-card__title">{{ service.title }}</h3>
          <p class="service-card__description">{{ service.description }}</p>
          <ul class="service-card__features">
            <li v-for="feature in service.features" :key="feature">{{ feature }}</li>
          </ul>
          <div class="service-card__footer">
            <span class="service-card__duration">{{ service.duration }}</span>
            <span class="service-card__price">{{ service.price }}</span>
          </div>
        </div>
      </div>
      
      <div class="services__modalities">
        <h3 class="services__modalities-title">Modalidades de Atendimento</h3>
        <div class="modalities">
          <div class="modality">
            <div class="modality__icon">🏢</div>
            <h4 class="modality__title">Presencial</h4>
            <p class="modality__description">
              Consultas no consultório, num ambiente acolhedor e confidencial, 
              localizado no centro da cidade com fácil acesso.
            </p>
          </div>
          <div class="modality">
            <div class="modality__icon">💻</div>
            <h4 class="modality__title">Online</h4>
            <p class="modality__description">
              Sessões por videochamada, oferecendo a mesma qualidade de atendimento 
              com a comodidade de estar em casa.
            </p>
          </div>
          <div class="modality">
            <div class="modality__icon">📱</div>
            <h4 class="modality__title">Híbrida</h4>
            <p class="modality__description">
              Combinação flexível entre consultas presenciais e online, 
              adaptando-se às suas necessidades e disponibilidade.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    id: 1,
    icon: '👤',
    title: 'Terapia Individual',
    description: 'Acompanhamento personalizado para adultos que enfrentam desafios emocionais, ansiedade, depressão ou questões de autoestima.',
    features: [
      'Avaliação psicológica inicial',
      'Plano terapêutico personalizado',
      'Técnicas cognitivo-comportamentais',
      'Acompanhamento contínuo'
    ],
    duration: '50 min',
    price: 'A partir de €60'
  },
  {
    id: 2,
    icon: '👥',
    title: 'Terapia de Casal',
    description: 'Apoio especializado para casais que desejam melhorar a comunicação, resolver conflitos e fortalecer a relação.',
    features: [
      'Análise da dinâmica do casal',
      'Técnicas de comunicação',
      'Resolução de conflitos',
      'Fortalecimento da intimidade'
    ],
    duration: '60 min',
    price: 'A partir de €80'
  },
  {
    id: 3,
    icon: '👨‍👩‍👧‍👦',
    title: 'Terapia Familiar',
    description: 'Intervenção terapêutica para famílias que enfrentam dificuldades de relacionamento ou períodos de transição.',
    features: [
      'Dinâmicas familiares',
      'Mediação de conflitos',
      'Comunicação eficaz',
      'Fortalecimento de vínculos'
    ],
    duration: '60 min',
    price: 'A partir de €90'
  },
  {
    id: 4,
    icon: '🧘‍♀️',
    title: 'Gestão do Stress',
    description: 'Técnicas especializadas para lidar com o stress, ansiedade e burnout, promovendo o equilíbrio emocional.',
    features: [
      'Técnicas de relaxamento',
      'Mindfulness e meditação',
      'Gestão do tempo',
      'Estratégias de coping'
    ],
    duration: '50 min',
    price: 'A partir de €65'
  },
  {
    id: 5,
    icon: '💼',
    title: 'Psicologia Organizacional',
    description: 'Consultoria para empresas focada no bem-estar dos colaboradores e melhoria do ambiente de trabalho.',
    features: [
      'Avaliação organizacional',
      'Workshops de bem-estar',
      'Gestão de conflitos',
      'Desenvolvimento de equipas'
    ],
    duration: 'Variável',
    price: 'Orçamento personalizado'
  },
  {
    id: 6,
    icon: '🎓',
    title: 'Orientação Vocacional',
    description: 'Apoio na descoberta de aptidões e interesses para escolhas acadêmicas e profissionais mais assertivas.',
    features: [
      'Testes vocacionais',
      'Análise de competências',
      'Exploração de carreiras',
      'Plano de desenvolvimento'
    ],
    duration: '50 min',
    price: 'A partir de €70'
  }
]
</script>

<style scoped>
.services {
  background-color: var(--white);
}

.services__grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-2xl);
}

.service-card {
  background-color: var(--white);
  border: 1px solid rgba(48, 56, 41, 0.1);
  border-radius: 16px;
  padding: var(--spacing-xl);
  transition: all var(--transition-normal);
  position: relative;
  overflow: hidden;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, var(--accent-color), var(--primary-color));
  transform: scaleX(0);
  transition: transform var(--transition-normal);
}

.service-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.service-card:hover::before {
  transform: scaleX(1);
}

.service-card__icon {
  font-size: 3rem;
  margin-bottom: var(--spacing-md);
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  background-color: var(--light-gray);
  border-radius: 50%;
  margin-left: auto;
  margin-right: auto;
}

.service-card__title {
  font-size: var(--font-size-xl);
  font-weight: 600;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: var(--spacing-md);
}

.service-card__description {
  color: var(--neutral-color);
  line-height: 1.6;
  margin-bottom: var(--spacing-lg);
  text-align: center;
}

.service-card__features {
  list-style: none;
  padding: 0;
  margin-bottom: var(--spacing-lg);
}

.service-card__features li {
  position: relative;
  padding-left: var(--spacing-lg);
  margin-bottom: var(--spacing-xs);
  color: var(--neutral-color);
  font-size: var(--font-size-small);
}

.service-card__features li::before {
  content: '✓';
  position: absolute;
  left: 0;
  color: var(--accent-color);
  font-weight: bold;
}

.service-card__footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: var(--spacing-md);
  border-top: 1px solid rgba(48, 56, 41, 0.1);
}

.service-card__duration {
  color: var(--neutral-color);
  font-size: var(--font-size-small);
}

.service-card__price {
  color: var(--accent-color);
  font-weight: 600;
  font-size: var(--font-size-base);
}

.services__modalities {
  margin-top: var(--spacing-2xl);
  padding-top: var(--spacing-2xl);
  border-top: 1px solid rgba(48, 56, 41, 0.1);
}

.services__modalities-title {
  font-size: var(--font-size-2xl);
  font-weight: 600;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: var(--spacing-xl);
}

.modalities {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--spacing-lg);
}

.modality {
  text-align: center;
  padding: var(--spacing-xl);
  background-color: var(--light-gray);
  border-radius: 16px;
  transition: transform var(--transition-normal);
}

.modality:hover {
  transform: translateY(-4px);
}

.modality__icon {
  font-size: 3rem;
  margin-bottom: var(--spacing-md);
}

.modality__title {
  font-size: var(--font-size-xl);
  font-weight: 600;
  color: var(--primary-color);
  margin-bottom: var(--spacing-md);
}

.modality__description {
  color: var(--neutral-color);
  line-height: 1.6;
}

/* Responsividade */
@media (max-width: 768px) {
  .services__grid {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
  
  .service-card {
    padding: var(--spacing-lg);
  }
  
  .modalities {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
  
  .modality {
    padding: var(--spacing-lg);
  }
}

@media (max-width: 480px) {
  .service-card__title,
  .modality__title {
    font-size: var(--font-size-large);
  }
  
  .services__modalities-title {
    font-size: var(--font-size-xl);
  }
}
</style>

