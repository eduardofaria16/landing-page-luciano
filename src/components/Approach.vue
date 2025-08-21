<template>
  <section id="abordagem" class="approach section">
    <div class="container">
      <h2 class="section-title">Abordagem Terapêutica</h2>
      <p class="section-subtitle">
        Utilizo métodos científicos comprovados, adaptados às necessidades únicas de cada pessoa
      </p>
      
      <div class="approach__content">
        <div class="approach__methods">
          <div class="method-card" v-for="method in methods" :key="method.id">
            <div class="method-card__header">
              <div class="method-card__icon">{{ method.icon }}</div>
              <h3 class="method-card__title">{{ method.title }}</h3>
            </div>
            <p class="method-card__description">{{ method.description }}</p>
            <ul class="method-card__benefits">
              <li v-for="benefit in method.benefits" :key="benefit">{{ benefit }}</li>
            </ul>
          </div>
        </div>
        
        <div class="approach__process">
          <h3 class="approach__process-title">Como Funciona o Processo Terapêutico</h3>
          <div class="process-steps">
            <div class="process-step" v-for="(step, index) in processSteps" :key="step.id">
              <div class="process-step__number">{{ index + 1 }}</div>
              <div class="process-step__content">
                <h4 class="process-step__title">{{ step.title }}</h4>
                <p class="process-step__description">{{ step.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <div class="approach__benefits">
        <h3 class="approach__benefits-title">Benefícios da Terapia</h3>
        <div class="benefits-grid">
          <div class="benefit-item" v-for="benefit in therapyBenefits" :key="benefit.id">
            <div class="benefit-item__icon">{{ benefit.icon }}</div>
            <h4 class="benefit-item__title">{{ benefit.title }}</h4>
            <p class="benefit-item__description">{{ benefit.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const methods = [
  {
    id: 1,
    icon: '🧠',
    title: 'Terapia Cognitivo-Comportamental',
    description: 'Abordagem focada na identificação e modificação de padrões de pensamento e comportamento que causam sofrimento.',
    benefits: [
      'Identificação de pensamentos disfuncionais',
      'Desenvolvimento de estratégias de coping',
      'Mudança de comportamentos problemáticos',
      'Resultados comprovados cientificamente'
    ]
  },
  {
    id: 2,
    icon: '❤️',
    title: 'Abordagem Humanística',
    description: 'Centrada na pessoa, valorizando a experiência individual e promovendo o crescimento pessoal e a autoaceitação.',
    benefits: [
      'Foco no potencial humano',
      'Ambiente não-julgamental',
      'Desenvolvimento da autoestima',
      'Promoção da autenticidade'
    ]
  },
  {
    id: 3,
    icon: '🧘',
    title: 'Mindfulness e ACT',
    description: 'Técnicas de atenção plena e Terapia de Aceitação e Compromisso para lidar com pensamentos e emoções difíceis.',
    benefits: [
      'Redução do stress e ansiedade',
      'Maior consciência emocional',
      'Aceitação de experiências difíceis',
      'Foco nos valores pessoais'
    ]
  }
]

const processSteps = [
  {
    id: 1,
    title: 'Primeira Consulta',
    description: 'Conhecimento mútuo, compreensão das suas necessidades e estabelecimento de objetivos terapêuticos.'
  },
  {
    id: 2,
    title: 'Avaliação',
    description: 'Análise aprofundada da situação atual, histórico pessoal e identificação de padrões comportamentais.'
  },
  {
    id: 3,
    title: 'Plano Terapêutico',
    description: 'Desenvolvimento de um plano personalizado com estratégias e técnicas adequadas ao seu caso.'
  },
  {
    id: 4,
    title: 'Acompanhamento',
    description: 'Sessões regulares com monitorização do progresso e ajustes no plano conforme necessário.'
  },
  {
    id: 5,
    title: 'Consolidação',
    description: 'Fortalecimento das competências adquiridas e preparação para a autonomia emocional.'
  }
]

const therapyBenefits = [
  {
    id: 1,
    icon: '🎯',
    title: 'Maior Autoconhecimento',
    description: 'Compreenda melhor os seus padrões de pensamento, emoções e comportamentos.'
  },
  {
    id: 2,
    icon: '💪',
    title: 'Desenvolvimento de Competências',
    description: 'Aprenda ferramentas práticas para lidar com desafios e situações stressantes.'
  },
  {
    id: 3,
    icon: '🌈',
    title: 'Melhoria das Relações',
    description: 'Desenvolva habilidades de comunicação e relacionamento mais saudáveis.'
  },
  {
    id: 4,
    icon: '⚖️',
    title: 'Equilíbrio Emocional',
    description: 'Encontre estabilidade emocional e aprenda a gerir melhor as suas emoções.'
  },
  {
    id: 5,
    icon: '🚀',
    title: 'Crescimento Pessoal',
    description: 'Descubra o seu potencial e trabalhe para alcançar os seus objetivos de vida.'
  },
  {
    id: 6,
    icon: '🛡️',
    title: 'Resiliência',
    description: 'Desenvolva a capacidade de se adaptar e recuperar de adversidades.'
  }
]
</script>

<style scoped>
.approach {
  background-color: var(--light-gray);
}

.approach__content {
  margin-bottom: var(--spacing-2xl);
}

.approach__methods {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-2xl);
}

.method-card {
  background-color: var(--white);
  border-radius: 16px;
  padding: var(--spacing-xl);
  box-shadow: var(--shadow-sm);
  transition: all var(--transition-normal);
  border-left: 4px solid var(--accent-color);
}

.method-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
}

.method-card__header {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  margin-bottom: var(--spacing-md);
}

.method-card__icon {
  font-size: 2.5rem;
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--light-gray);
  border-radius: 50%;
  flex-shrink: 0;
}

.method-card__title {
  font-size: var(--font-size-xl);
  font-weight: 600;
  color: var(--primary-color);
  margin: 0;
}

.method-card__description {
  color: var(--neutral-color);
  line-height: 1.6;
  margin-bottom: var(--spacing-lg);
}

.method-card__benefits {
  list-style: none;
  padding: 0;
  margin: 0;
}

.method-card__benefits li {
  position: relative;
  padding-left: var(--spacing-lg);
  margin-bottom: var(--spacing-xs);
  color: var(--neutral-color);
  font-size: var(--font-size-small);
}

.method-card__benefits li::before {
  content: '✓';
  position: absolute;
  left: 0;
  color: var(--accent-color);
  font-weight: bold;
}

.approach__process {
  background-color: var(--white);
  border-radius: 16px;
  padding: var(--spacing-xl);
  box-shadow: var(--shadow-sm);
}

.approach__process-title {
  font-size: var(--font-size-2xl);
  font-weight: 600;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: var(--spacing-xl);
}

.process-steps {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.process-step {
  display: flex;
  align-items: flex-start;
  gap: var(--spacing-md);
  position: relative;
}

.process-step:not(:last-child)::after {
  content: '';
  position: absolute;
  left: 24px;
  top: 60px;
  width: 2px;
  height: calc(100% + var(--spacing-lg));
  background-color: var(--accent-color);
  opacity: 0.3;
}

.process-step__number {
  width: 48px;
  height: 48px;
  background-color: var(--accent-color);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: var(--font-size-large);
  flex-shrink: 0;
}

.process-step__content {
  flex: 1;
  padding-top: var(--spacing-xs);
}

.process-step__title {
  font-size: var(--font-size-large);
  font-weight: 600;
  color: var(--primary-color);
  margin: 0 0 var(--spacing-xs) 0;
}

.process-step__description {
  color: var(--neutral-color);
  line-height: 1.6;
  margin: 0;
}

.approach__benefits {
  background-color: var(--white);
  border-radius: 16px;
  padding: var(--spacing-xl);
  box-shadow: var(--shadow-sm);
}

.approach__benefits-title {
  font-size: var(--font-size-2xl);
  font-weight: 600;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: var(--spacing-xl);
}

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--spacing-lg);
}

.benefit-item {
  text-align: center;
  padding: var(--spacing-lg);
  border-radius: 12px;
  transition: transform var(--transition-normal);
}

.benefit-item:hover {
  transform: translateY(-4px);
  background-color: var(--light-gray);
}

.benefit-item__icon {
  font-size: 2.5rem;
  margin-bottom: var(--spacing-md);
}

.benefit-item__title {
  font-size: var(--font-size-large);
  font-weight: 600;
  color: var(--primary-color);
  margin: 0 0 var(--spacing-sm) 0;
}

.benefit-item__description {
  color: var(--neutral-color);
  line-height: 1.6;
  margin: 0;
}

/* Responsividade */
@media (max-width: 768px) {
  .approach__methods {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
  
  .method-card,
  .approach__process,
  .approach__benefits {
    padding: var(--spacing-lg);
  }
  
  .benefits-grid {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
  
  .process-step {
    flex-direction: column;
    text-align: center;
  }
  
  .process-step:not(:last-child)::after {
    display: none;
  }
}

@media (max-width: 480px) {
  .method-card__header {
    flex-direction: column;
    text-align: center;
  }
  
  .approach__process-title,
  .approach__benefits-title {
    font-size: var(--font-size-xl);
  }
}
</style>

