<template>
  <section id="servicos" class="services section">
    <div class="container">
      
      <!-- Hero Header -->
      <div class="services-hero">
        <h2 class="hero-title">Nossos Serviços</h2>
        <p class="hero-subtitle">
          Um pouco do nosso trabalho e como impactamos os nossos clientes e pacientes a sentir uma experiência única
        </p>
        <div class="hero-decoration">
          <div class="decoration-line"></div>
          <div class="decoration-dot"></div>
          <div class="decoration-line"></div>
        </div>
      </div>
      
      <!-- Cards de Serviços com Layout Inovador -->
      <div class="services-showcase">
        <div 
          class="service-card-modern" 
          v-for="(service, index) in services" 
          :key="service.id"
          :class="{ 'featured': index === 1 }"
          :style="{ '--card-index': index }"
        >
          <div class="card-background-effect"></div>
          
          <div class="card-header">
            <div class="service-icon-container">
              <span class="service-icon">{{ service.icon }}</span>
              <div class="icon-glow"></div>
            </div>
            <h3 class="service-title">{{ service.title }}</h3>
          </div>
          
          <div class="card-body">
            <!-- Se for um card de lista -->
            <div v-if="service.features" class="features-grid">
              <div 
                class="feature-item" 
                v-for="(feature, featureIndex) in service.features" 
                :key="featureIndex"
                :style="{ '--feature-delay': featureIndex * 0.1 + 's' }"
              >
                <div class="feature-check">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M20 6L9 17L4 12" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
                  </svg>
                </div>
                <span class="feature-text">{{ feature }}</span>
              </div>
            </div>

            <!-- Se for um card de lançamentos com imagem -->
            <div v-else-if="service.image" class="launch-image">
              <img :src="service.image" alt="Capa do Livro" />
            </div>
          </div>
          
          <div class="card-shine"></div>
        </div>
      </div>

      <!-- Modalidades com Design Futurista -->
      <div class="modalities-section">
        <div class="modalities-header">
          <h3 class="modalities-title">Modalidades de Atendimento</h3>
          <p class="modalities-subtitle">Flexibilidade para atender você onde estiver</p>
        </div>
        
        <div class="modalities-container">
          <div class="modality-card">
            <div class="modality-visual">
              <div class="modality-icon-wrapper">
                <span class="modality-icon">💻</span>
                <div class="pulse-ring-1"></div>
                <div class="pulse-ring-2"></div>
                <div class="pulse-ring-3"></div>
              </div>
            </div>
            
            <div class="modality-content">
              <h4 class="modality-title">Atendimento Online</h4>
              <p class="modality-description">
                Atendimento on-line para o Brasil e Exterior com toda segurança e privacidade
              </p>
              
              <div class="modality-benefits">
                <div class="benefit-tag">🌍 Acesso Global</div>
                <div class="benefit-tag">🔒 100% Seguro</div>
                <div class="benefit-tag">⏰ Flexível</div>
              </div>
            </div>
            
            <div class="modality-decoration">
              <div class="decoration-particles">
                <div class="particle" style="--delay: 0s; --x: 20px; --y: 30px;"></div>
                <div class="particle" style="--delay: 0.5s; --x: 60px; --y: 20px;"></div>
                <div class="particle" style="--delay: 1s; --x: 40px; --y: 50px;"></div>
                <div class="particle" style="--delay: 1.5s; --x: 80px; --y: 40px;"></div>
              </div>
            </div>
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
    icon: '🧠',
    title: 'Psicologia Clínica',
    features: [
      'Ansiedade, Burnout e Transtorno de Estresse Pós-Traumático',
      'Depressão e demais Transtornos Psicológicos',
      'Conflitos relacionais entre casais, pais e filhos',
      'Lutos e Encerramento de ciclos',
      'Autoestima e Desenvolvimento Pessoal',
      'Orientação Profissional e Gestão de Carreiras',
    ],
  },
  {
    id: 2,
    icon: '💼',
    title: 'Psicologia Para Organizações e Trabalho',
    features: [
      'Inteligência Emocional no Ambiente Corporativo – Como desenvolver autoconsciência, empatia e gestão emocional para melhores resultados.',
      'Gestão do Estresse e Prevenção do Burnout – Estratégias para equilíbrio emocional e produtividade saudável.',      
      'Comunicação Assertiva e Feedback Construtivo – Técnicas para melhorar o diálogo e reduzir conflitos internos.',
      'Gestão de Conflitos e Cultura Colaborativa – Métodos para transformar divergências em oportunidades de crescimento.',
      'Saúde Mental e Qualidade de Vida no Trabalho – Programas para promover equilíbrio entre vida pessoal e profissional.',
    ],
  },
  {
    id: 3,
    icon: '📚',
    title: 'Psicologia Escolar',
    features: [
      'Desenvolvimento Socioemocional de Alunos – Estratégias para fortalecer empatia, autorregulação, resiliência e habilidades sociais.',
      'Carreira e Trabalho: Como me organizar para a vida adulta',
      'Saúde Mental e Autocuidado para Educadores – Técnicas para prevenir estresse e burnout na equipe escolar.',
      'Mediação de Conflitos e Cultura de Paz – Métodos para lidar com conflitos entre alunos, pais e professores.',
      'Prevenção ao Bullying e Cyberbullying – Ações para identificar, intervir e conscientizar sobre a violência escolar.',
      'Inclusão e Diversidade na Escola – Práticas para promover acolhimento e respeito às diferenças.',
      'Comunicação Eficaz Escola-Família – Ferramentas para melhorar o relacionamento com pais e responsáveis.',
      'Burnout Escolar e Acadêmico-Universitário',
    ],
  },
  {
    id: 4,
    icon: '🚀',
    title: 'Lançamentos e Publicações',
    image: '/src/assets/capa-livro.png',
  },
]
</script>

<style scoped>
.launch-image {
  display: flex;
  justify-content: center;
  margin-top: 60px;
}

.launch-image img {
  max-width: 480px; /* tamanho máximo */
  border-radius: 15px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  transition: transform 0.3s ease;
}

.launch-image img:hover {
  transform: scale(1.05);
}

.services {
  background: linear-gradient(180deg, #f8f9f7 0%, #ffffff 50%, #f5f6f4 100%);
  padding: 80px 0;
  position: relative;
  overflow: hidden;
}

.services::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(209, 133, 82, 0.06) 0%, transparent 50%),
    radial-gradient(circle at 85% 75%, rgba(48, 56, 41, 0.04) 0%, transparent 50%),
    radial-gradient(circle at 50% 50%, rgba(145, 144, 126, 0.03) 0%, transparent 70%);
  pointer-events: none;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  position: relative;
  z-index: 1;
}

/* Hero Header */
.services-hero {
  text-align: center;
  margin-bottom: 80px;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: 20px;
  position: relative;
}

.hero-subtitle {
  font-size: 1.2rem;
  color: var(--secondary-color);
  max-width: 600px;
  margin: 0 auto 40px;
  line-height: 1.6;
  font-weight: 300;
}

.hero-decoration {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  margin-top: 30px;
}

.decoration-line {
  width: 60px;
  height: 2px;
  background: linear-gradient(90deg, transparent 0%, var(--accent-color) 50%, transparent 100%);
}

.decoration-dot {
  width: 8px;
  height: 8px;
  background: var(--accent-color);
  border-radius: 50%;
  animation: pulse-dot 2s ease-in-out infinite;
}

@keyframes pulse-dot {
  0%, 100% { transform: scale(1); opacity: 1; }
  50% { transform: scale(1.2); opacity: 0.8; }
}

/* Cards de Serviços */
.services-showcase {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
  gap: 40px;
  margin-bottom: 100px;
}

.service-card-modern {
  position: relative;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(48, 56, 41, 0.08);
  border-radius: 25px;
  padding: 40px 30px;
  transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
  overflow: hidden;
  animation: slideInUp 0.8s ease-out forwards;
  animation-delay: calc(var(--card-index) * 0.2s);
  opacity: 0;
  transform: translateY(50px);
}

@keyframes slideInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.service-card-modern:hover {
  transform: translateY(-15px) scale(1.02);
  box-shadow: 0 25px 50px rgba(48, 56, 41, 0.15);
  border-color: rgba(209, 133, 82, 0.2);
}

.service-card-modern.featured {
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.05) 0%, rgba(255, 255, 255, 0.95) 100%);
  border: 2px solid rgba(209, 133, 82, 0.15);
  transform: scale(1.05);
}

.service-card-modern.featured:hover {
  transform: translateY(-15px) scale(1.07);
}

.card-background-effect {
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: conic-gradient(from 0deg, transparent 0deg, rgba(209, 133, 82, 0.05) 90deg, transparent 180deg);
  animation: rotate 20s linear infinite;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.service-card-modern:hover .card-background-effect {
  opacity: 1;
}

@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.card-header {
  text-align: center;
  margin-bottom: 35px;
}

.service-icon-container {
  position: relative;
  display: inline-block;
  margin-bottom: 25px;
}

.service-icon {
  font-size: 3.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100px;
  height: 100px;
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.1) 0%, rgba(48, 56, 41, 0.05) 100%);
  border-radius: 50%;
  border: 3px solid rgba(209, 133, 82, 0.1);
  transition: all 0.3s ease;
  position: relative;
  z-index: 2;
}

.service-card-modern:hover .service-icon {
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.15) 0%, rgba(48, 56, 41, 0.1) 100%);
  border-color: rgba(209, 133, 82, 0.3);
  transform: scale(1.1);
}

.icon-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 120px;
  height: 120px;
  background: radial-gradient(circle, rgba(209, 133, 82, 0.1) 0%, transparent 70%);
  border-radius: 50%;
  opacity: 0;
  transition: opacity 0.3s ease;
  animation: glow-pulse 3s ease-in-out infinite;
}

.service-card-modern:hover .icon-glow {
  opacity: 1;
}

@keyframes glow-pulse {
  0%, 100% { transform: translate(-50%, -50%) scale(1); opacity: 0.5; }
  50% { transform: translate(-50%, -50%) scale(1.1); opacity: 0.8; }
}

.service-title {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--primary-color);
  margin: 0;
  line-height: 1.3;
}

.card-body {
  position: relative;
}

.features-grid {
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  opacity: 0;
  animation: fadeInLeft 0.6s ease-out forwards;
  animation-delay: calc(var(--feature-delay) + 0.3s);
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.feature-check {
  width: 20px;
  height: 20px;
  background: linear-gradient(135deg, var(--accent-color) 0%, #b8734a 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  flex-shrink: 0;
  margin-top: 2px;
  transition: transform 0.2s ease;
}

.feature-check svg {
  width: 12px;
  height: 12px;
}

.feature-item:hover .feature-check {
  transform: scale(1.1);
}

.feature-text {
  color: var(--secondary-color);
  line-height: 1.5;
  font-size: 0.95rem;
}

.card-shine {
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
  transition: left 0.6s ease;
  pointer-events: none;
}

.service-card-modern:hover .card-shine {
  left: 100%;
}

/* Modalidades */
.modalities-section {
  position: relative;
  background: linear-gradient(135deg, rgba(48, 56, 41, 0.03) 0%, rgba(209, 133, 82, 0.02) 100%);
  border-radius: 30px;
  padding: 60px 40px;
  border: 1px solid rgba(48, 56, 41, 0.05);
}

.modalities-header {
  text-align: center;
  margin-bottom: 50px;
}

.modalities-title {
  font-size: 2.5rem;
  font-weight: 600;
  color: var(--primary-color);
  margin-bottom: 15px;
}

.modalities-subtitle {
  font-size: 1.1rem;
  color: var(--secondary-color);
  font-weight: 300;
}

.modalities-container {
  max-width: 800px;
  margin: 0 auto;
}

.modality-card {
  position: relative;
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(209, 133, 82, 0.1);
  border-radius: 25px;
  padding: 50px 40px;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  overflow: hidden;
}

.modality-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 30px 60px rgba(48, 56, 41, 0.1);
  border-color: rgba(209, 133, 82, 0.2);
}

.modality-visual {
  text-align: center;
  margin-bottom: 30px;
  position: relative;
}

.modality-icon-wrapper {
  position: relative;
  display: inline-block;
}

.modality-icon {
  font-size: 4rem;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 120px;
  height: 120px;
  background: linear-gradient(135deg, var(--accent-color) 0%, #b8734a 100%);
  border-radius: 50%;
  color: white;
  position: relative;
  z-index: 3;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.pulse-ring-1, .pulse-ring-2, .pulse-ring-3 {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border: 2px solid rgba(209, 133, 82, 0.3);
  border-radius: 50%;
  animation: pulse-ring 3s ease-out infinite;
}

.pulse-ring-1 {
  width: 140px;
  height: 140px;
  animation-delay: 0s;
}

.pulse-ring-2 {
  width: 160px;
  height: 160px;
  animation-delay: 0.7s;
}

.pulse-ring-3 {
  width: 180px;
  height: 180px;
  animation-delay: 1.4s;
}

@keyframes pulse-ring {
  0% {
    transform: translate(-50%, -50%) scale(0.8);
    opacity: 1;
  }
  100% {
    transform: translate(-50%, -50%) scale(1.2);
    opacity: 0;
  }
}

.modality-content {
  text-align: center;
}

.modality-title {
  font-size: 1.8rem;
  font-weight: 600;
  color: var(--primary-color);
  margin-bottom: 20px;
}

.modality-description {
  font-size: 1.1rem;
  color: var(--secondary-color);
  line-height: 1.6;
  margin-bottom: 30px;
}

.modality-benefits {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px;
}

.benefit-tag {
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.1) 0%, rgba(48, 56, 41, 0.05) 100%);
  color: var(--primary-color);
  padding: 10px 20px;
  border-radius: 25px;
  font-size: 0.9rem;
  font-weight: 500;
  border: 1px solid rgba(209, 133, 82, 0.1);
  transition: all 0.3s ease;
}

.benefit-tag:hover {
  background: linear-gradient(135deg, rgba(209, 133, 82, 0.15) 0%, rgba(48, 56, 41, 0.08) 100%);
  transform: translateY(-2px);
  border-color: rgba(209, 133, 82, 0.2);
}

.modality-decoration {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  pointer-events: none;
  overflow: hidden;
}

.decoration-particles {
  position: relative;
  width: 100%;
  height: 100%;
}

.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  background: var(--accent-color);
  border-radius: 50%;
  opacity: 0;
  animation: float-particle 4s ease-in-out infinite;
  animation-delay: var(--delay);
  left: var(--x);
  top: var(--y);
}

@keyframes float-particle {
  0%, 100% {
    opacity: 0;
    transform: translateY(0px) scale(1);
  }
  20%, 80% {
    opacity: 0.6;
  }
  50% {
    opacity: 1;
    transform: translateY(-20px) scale(1.2);
  }
}

/* Responsividade */
@media (max-width: 768px) {
  .services-showcase {
    grid-template-columns: 1fr;
    gap: 30px;
  }
  
  .service-card-modern.featured {
    transform: none;
  }
  
  .service-card-modern.featured:hover {
    transform: translateY(-15px) scale(1.02);
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .modalities-title {
    font-size: 2rem;
  }
  
  .modality-card {
    padding: 40px 30px;
  }
  
  .modality-benefits {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 0 15px;
  }
  
  .services {
    padding: 60px 0;
  }
  
  .service-card-modern,
  .modalities-section {
    padding: 30px 20px;
  }
  
  .hero-title {
    font-size: 2rem;
  }
  
  .service-icon {
    width: 80px;
    height: 80px;
    font-size: 2.5rem;
  }
  
  .modality-icon {
    width: 100px;
    height: 100px;
    font-size: 3rem;
  }
  
  .benefit-tag {
    font-size: 0.8rem;
    padding: 8px 15px;
  }
}
</style>