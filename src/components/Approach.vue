<template>
  <section id="abordagem" class="approach section">
    <div class="container">
      
      <!-- Hero Section com Timeline Interativo -->
      <div class="therapy-journey">
        <h2 class="journey-title">Jornada Terapêutica Humanista</h2>
        <p class="journey-subtitle">Uma abordagem centrada na pessoa para o seu crescimento</p>
        
        <!-- Timeline Principal -->
        <div class="timeline-container">
          <div class="timeline-line"></div>
          <div class="timeline-steps">
            <div 
              class="timeline-step" 
              v-for="(step, index) in processSteps" 
              :key="step.id"
              :class="{ 'active': activeStep === index }"
              @click="setActiveStep(index)"
            >
              <div class="timeline-dot">
                <div class="timeline-dot-inner">{{ index + 1 }}</div>
              </div>
              <div class="timeline-content">
                <h3 class="timeline-title">{{ step.title }}</h3>
                <p class="timeline-description">{{ step.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Cards Flutuantes - Como Ocorre o Processo -->
      <div class="floating-cards-section">
        <h2 class="section-title">Como Ocorre o Processo</h2>
        <div class="floating-cards">
          <div 
            class="floating-card" 
            v-for="(step, index) in processSteps2" 
            :key="step.id"
            :style="{ '--delay': index * 0.2 + 's' }"
          >
            <div class="card-number">{{ index + 1 }}</div>
            <div class="card-content">
              <h3 class="card-title">{{ step.title }}</h3>
              <p class="card-description">{{ step.description }}</p>
            </div>
            <div class="card-glow"></div>
          </div>
        </div>
      </div>

      <!-- Seção Foco no Presente - Design Minimalista -->
      <div class="present-focus">
        <div class="present-focus-content">
          <h2 class="present-title">Foco no Presente</h2>
          <div class="present-grid">
            <div class="present-item" v-for="(step, index) in processSteps3" :key="step.id">
              <div class="present-icon">
                <div class="pulse-ring"></div>
                <span>{{ index + 1 }}</span>
              </div>
              <div class="present-text">
                <h3 v-if="step.title" class="present-item-title">{{ step.title }}</h3>
                <p class="present-description">{{ step.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Benefícios com Design de Grid Moderno -->
      <div class="benefits-modern">
        <h2 class="benefits-title">Transformação Através da Terapia</h2>
        <div class="benefits-grid-modern">
          <div 
            class="benefit-card-modern" 
            v-for="(benefit, index) in therapyBenefits" 
            :key="benefit.id"
            :style="{ '--index': index }"
          >
            <div class="benefit-icon-container">
              <span class="benefit-icon">{{ benefit.icon }}</span>
              <div class="benefit-icon-bg"></div>
            </div>
            <h3 class="benefit-title">{{ benefit.title }}</h3>
            <p class="benefit-description">{{ benefit.description }}</p>
            <div class="benefit-hover-effect"></div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeStep = ref(0)

const setActiveStep = (index) => {
  activeStep.value = index
}

const processSteps = [
  {
    id: 1,
    title: 'Harmonia e Autenticidade',
    description: 'O terapeuta se mostra genuíno e autêntico, o que permite ao paciente sentir-se seguro para explorar seu próprio "eu" de forma aberta e sem receios.'
  },
  {
    id: 2,
    title: 'Empatia e Compreensão',
    description: 'O terapeuta se esforça para compreender o mundo do paciente a partir da perspectiva dele, comunicando essa compreensão ao paciente.'
  },
  {
    id: 3,
    title: 'Aceitação Incondicional',
    description: 'O terapeuta acolhe o paciente sem julgamentos, valorizando-o como ser humano e criando um espaço seguro para a expressão de seus sentimentos, pensamentos e experiências.'
  },
  {
    id: 4,
    title: 'Autoconhecimento e Autorrealização',
    description: 'À medida que o paciente se sente acolhido e compreendido, ele começa a se autoavaliar, tomar consciência de seus padrões de comportamento e emoções, e a desenvolver a aceitação de si mesmo, caminhando para a sua plena realização.'
  },
]

const processSteps2 = [
  {
    id: 1,
    title: 'Diálogo e Expressão',
    description: 'O processo ocorre através da conversa, onde o cliente é encorajado a expressar seus sentimentos e pensamentos, fortalecendo a relação terapêutica.'
  },
  {
    id: 2,
    title: 'Auto-observação',
    description: 'O paciente aprende a se observar, a reconhecer seus padrões de comportamento e a identificar como suas experiências passadas e crenças limitantes afetam seu presente.'
  },
  {
    id: 3,
    title: 'Desenvolvimento da Autoconsciência',
    description: 'A terapia visa promover o autoconhecimento e o desenvolvimento do autoconceito, que é a percepção de si mesmo, incluindo a autoimagem, autoestima e o "eu ideal".'
  },
]

const processSteps3 = [
  {
    id: 1,
    description: 'Embora o passado seja explorado, o foco do humanismo está na experiência presente do paciente e no seu potencial para crescer e se autorrealizar.'
  },
  {
    id: 2,
    title: 'O Resultado',
    description: 'O objetivo final é que o indivíduo se desenvolva de forma mais completa e autêntica, alcançando maior equilíbrio emocional e autonomia perante à vida e bem-estar através da própria experiência terapêutica.'
  },
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
    icon: '🤝',
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
  background: linear-gradient(135deg, var(--primary-color) 0%, #2a3021 50%, var(--secondary-color) 100%);
  min-height: 100vh;
  padding: 60px 0;
  position: relative;
  overflow: hidden;
}

.approach::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 80%, rgba(209, 133, 82, 0.15) 0%, transparent 60%),
    radial-gradient(circle at 80% 20%, rgba(145, 144, 126, 0.12) 0%, transparent 60%),
    radial-gradient(circle at 40% 40%, rgba(209, 133, 82, 0.08) 0%, transparent 70%);
  pointer-events: none;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  position: relative;
  z-index: 1;
}

/* Timeline Interativo */
.therapy-journey {
  text-align: center;
  margin-bottom: 80px;
}

.journey-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: white;
  margin-bottom: 16px;
  text-shadow: 0 4px 20px rgba(0,0,0,0.3);
}

.journey-subtitle {
  font-size: 1.3rem;
  color: rgba(255,255,255,0.9);
  margin-bottom: 60px;
  font-weight: 300;
}

.timeline-container {
  position: relative;
  max-width: 800px;
  margin: 0 auto;
}

.timeline-line {
  position: absolute;
  top: 50px;
  left: 50%;
  transform: translateX(-50%);
  width: calc(100% - 100px);
  height: 3px;
  background: linear-gradient(90deg, rgba(255,255,255,0.3) 0%, white 50%, rgba(255,255,255,0.3) 100%);
  border-radius: 2px;
}

.timeline-steps {
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.timeline-step {
  display: flex;
  align-items: center;
  gap: 30px;
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  opacity: 0.7;
}

.timeline-step:nth-child(even) {
  flex-direction: row-reverse;
  text-align: right;
}

.timeline-step.active {
  opacity: 1;
  transform: scale(1.02);
}

.timeline-dot {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #fff 0%, #f0f0f0 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.2);
  transition: all 0.3s ease;
  flex-shrink: 0;
}

.timeline-step.active .timeline-dot {
  background: linear-gradient(135deg, var(--accent-color) 0%, #b8734a 100%);
  transform: scale(1.1);
  box-shadow: 0 15px 40px rgba(209, 133, 82, 0.4);
}

.timeline-dot-inner {
  font-size: 1.5rem;
  font-weight: 700;
  color: #333;
  transition: color 0.3s ease;
}

.timeline-step.active .timeline-dot-inner {
  color: white;
}

.timeline-content {
  flex: 1;
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(20px);
  padding: 25px;
  border-radius: 20px;
  border: 1px solid rgba(255,255,255,0.2);
  transition: all 0.3s ease;
}

.timeline-step.active .timeline-content {
  background: rgba(255,255,255,0.15);
  transform: translateY(-5px);
}

.timeline-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: white;
  margin-bottom: 12px;
}

.timeline-description {
  color: rgba(255,255,255,0.9);
  line-height: 1.6;
  font-size: 1rem;
}

/* Cards Flutuantes */
.floating-cards-section {
  margin-bottom: 80px;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 600;
  color: white;
  text-align: center;
  margin-bottom: 50px;
  text-shadow: 0 4px 20px rgba(0,0,0,0.3);
}

.floating-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 30px;
}

.floating-card {
  position: relative;
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(20px);
  border-radius: 25px;
  padding: 30px;
  border: 1px solid rgba(255,255,255,0.2);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  animation: floatIn 0.8s ease-out forwards;
  animation-delay: var(--delay, 0s);
  opacity: 0;
  transform: translateY(30px);
  overflow: hidden;
}

@keyframes floatIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.floating-card:hover {
  transform: translateY(-10px) scale(1.02);
  background: rgba(255,255,255,0.15);
}

.card-number {
  position: absolute;
  top: 20px;
  right: 20px;
  width: 40px;
  height: 40px;
  background: linear-gradient(135deg, var(--accent-color) 0%, #b8734a 100%);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.1rem;
}

.card-title {
  font-size: 1.3rem;
  font-weight: 600;
  color: white;
  margin-bottom: 15px;
}

.card-description {
  color: rgba(255,255,255,0.9);
  line-height: 1.6;
  font-size: 1rem;
}

.card-glow {
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
  opacity: 0;
  transition: opacity 0.3s ease;
  pointer-events: none;
}

.floating-card:hover .card-glow {
  opacity: 1;
}

/* Foco no Presente */
.present-focus {
  margin-bottom: 80px;
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(20px);
  border-radius: 30px;
  padding: 50px 30px;
  border: 1px solid rgba(255,255,255,0.1);
}

.present-title {
  font-size: 2.5rem;
  font-weight: 600;
  color: white;
  text-align: center;
  margin-bottom: 40px;
}

.present-grid {
  display: flex;
  flex-direction: column;
  gap: 30px;
  max-width: 600px;
  margin: 0 auto;
}

.present-item {
  display: flex;
  align-items: center;
  gap: 25px;
  text-align: left;
}

.present-icon {
  position: relative;
  width: 60px;
  height: 60px;
  background: linear-gradient(135deg, var(--accent-color) 0%, #b8734a 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: 700;
  flex-shrink: 0;
}

.pulse-ring {
  position: absolute;
  border: 3px solid rgba(209, 133, 82, 0.4);
  border-radius: 50%;
  width: 80px;
  height: 80px;
  animation: pulse 2s ease-out infinite;
}

@keyframes pulse {
  0% {
    transform: scale(0.8);
    opacity: 1;
  }
  100% {
    transform: scale(1.4);
    opacity: 0;
  }
}

.present-text {
  flex: 1;
}

.present-item-title {
  font-size: 1.2rem;
  font-weight: 600;
  color: white;
  margin-bottom: 8px;
}

.present-description {
  color: rgba(255,255,255,0.9);
  line-height: 1.6;
  font-size: 1rem;
}

/* Benefícios Modernos */
.benefits-modern {
  background: rgba(255,255,255,0.08);
  backdrop-filter: blur(30px);
  border-radius: 30px;
  padding: 50px 30px;
  border: 1px solid rgba(255,255,255,0.1);
}

.benefits-title {
  font-size: 2.5rem;
  font-weight: 600;
  color: white;
  text-align: center;
  margin-bottom: 50px;
  text-shadow: 0 4px 20px rgba(0,0,0,0.3);
}

.benefits-grid-modern {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
}

.benefit-card-modern {
  position: relative;
  background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.05) 100%);
  backdrop-filter: blur(20px);
  border-radius: 20px;
  padding: 30px 25px;
  border: 1px solid rgba(255,255,255,0.2);
  text-align: center;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  animation: slideInUp 0.6s ease-out forwards;
  animation-delay: calc(var(--index) * 0.1s);
  opacity: 0;
  transform: translateY(30px);
  overflow: hidden;
}

@keyframes slideInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.benefit-card-modern:hover {
  transform: translateY(-8px);
  background: linear-gradient(135deg, rgba(255,255,255,0.15) 0%, rgba(255,255,255,0.08) 100%);
}

.benefit-icon-container {
  position: relative;
  display: inline-flex;
  margin-bottom: 20px;
}

.benefit-icon {
  font-size: 2.5rem;
  position: relative;
  z-index: 2;
}

.benefit-icon-bg {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 70px;
  height: 70px;
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.2) 0%, rgba(184, 115, 74, 0.2) 100%);
  border-radius: 50%;
  transition: all 0.3s ease;
}

.benefit-card-modern:hover .benefit-icon-bg {
  transform: translate(-50%, -50%) scale(1.2);
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.35) 0%, rgba(184, 115, 74, 0.35) 100%);
}

.benefit-title {
  font-size: 1.2rem;
  font-weight: 600;
  color: white;
  margin-bottom: 12px;
}

.benefit-description {
  color: rgba(255,255,255,0.85);
  line-height: 1.5;
  font-size: 0.95rem;
}

.benefit-hover-effect {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, transparent 30%, rgba(255,255,255,0.1) 50%, transparent 70%);
  transform: translateX(-100%);
  transition: transform 0.6s ease;
}

.benefit-card-modern:hover .benefit-hover-effect {
  transform: translateX(100%);
}

/* Responsividade */
@media (max-width: 768px) {
  .journey-title {
    font-size: 2.5rem;
  }
  
  .timeline-step {
    flex-direction: column !important;
    text-align: center !important;
  }
  
  .timeline-line {
    display: none;
  }
  
  .floating-cards {
    grid-template-columns: 1fr;
  }
  
  .present-item {
    flex-direction: column;
    text-align: center;
  }
  
  .benefits-grid-modern {
    grid-template-columns: 1fr;
  }
  
  .section-title,
  .benefits-title,
  .present-title {
    font-size: 2rem;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 0 15px;
  }
  
  .timeline-content,
  .floating-card,
  .present-focus,
  .benefits-modern {
    padding: 25px 20px;
  }
  
  .journey-title {
    font-size: 2rem;
  }
}
</style>