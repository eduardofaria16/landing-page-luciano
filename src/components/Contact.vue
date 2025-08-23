<template>
  <section id="contato" class="contact section">
    <div class="container">
      <h2 class="section-title">Vamos Conversar?</h2>
      <p class="section-subtitle">
        Escolha a forma mais confortável para entrar em contato comigo
      </p>
      
      <div class="contact__cards">
        <!-- Card Instagram -->
        <div class="contact__card contact__card--instagram" @click="openInstagram">
          <div class="card__background">
            <div class="card__pattern"></div>
          </div>
          
          <div class="card__content">
            <div class="card__header">
              <div class="card__icon card__icon--instagram">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
              </div>
              <span class="card__badge">Siga-me</span>
            </div>
            
            <h3 class="card__title">Instagram</h3>
            <p class="card__description">
              Acompanhe dicas de bem-estar, reflexões sobre saúde mental e conteúdos exclusivos
            </p>
            
            <div class="card__features">
              <div class="feature__item">
                <span class="feature__icon">📸</span>
                <span>Conteúdo Diário</span>
              </div>
              <div class="feature__item">
                <span class="feature__icon">💡</span>
                <span>Dicas de Psicologia</span>
              </div>
            </div>
            
            <div class="card__username">
              @luciano.tarso
            </div>
            
            <div class="card__action">
              <span class="action__text">Toque para seguir</span>
              <div class="action__arrow">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M7 17l9.2-9.2M17 17H7V7"/>
                </svg>
              </div>
            </div>
          </div>
        </div>

        <!-- Card WhatsApp -->
        <div class="contact__card contact__card--whatsapp" @click="openWhatsApp">
          <div class="card__background">
            <div class="card__pattern card__pattern--whatsapp"></div>
          </div>
          
          <div class="card__content">
            <div class="card__header">
              <div class="card__icon card__icon--whatsapp">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.890-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/>
                </svg>
              </div>
              <span class="card__badge card__badge--primary">Consultas</span>
            </div>
            
            <h3 class="card__title">WhatsApp</h3>
            <p class="card__description">
              Agende sua consulta de forma rápida e segura. Atendimento personalizado e confidencial
            </p>
            
            <div class="card__features">
              <div class="feature__item">
                <span class="feature__icon">⚡</span>
                <span>Resposta Rápida</span>
              </div>
              <div class="feature__item">
                <span class="feature__icon">🔒</span>
                <span>100% Privado</span>
              </div>
            </div>
            
            <div class="card__phone">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
              </svg>
              +55 34 99687-7462
            </div>
            
            <div class="card__action">
              <span class="action__text">Toque para conversar</span>
              <div class="action__arrow">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M7 17l9.2-9.2M17 17H7V7"/>
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Informações adicionais -->
      <div class="contact__info">
        <div class="info__item">
          <div class="info__icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
              <polyline points="22,6 12,13 2,6"/>
            </svg>
          </div>
          <div class="info__content">
            <span class="info__label">Email</span>
            <span class="info__value">tarsoluciano@gmail.com</span>
          </div>
        </div>
        
        <div class="info__item">
          <div class="info__icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
              <circle cx="12" cy="10" r="3"/>
            </svg>
          </div>
          <div class="info__content">
            <span class="info__label">Localização</span>
            <span class="info__value">Uberlândia, MG</span>
          </div>
        </div>
        
        <div class="info__item">
          <div class="info__icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M12 1v6m0 0l4-4m-4 4L8 3m4 18v-6m0 0l4 4m-4-4l-4 4"/>
            </svg>
          </div>
          <div class="info__content">
            <span class="info__label">Modalidades</span>
            <span class="info__value">Online | Presencial sob consulta prévia </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const openWhatsApp = () => {
  const phoneNumber = "5534996877462"
  const message = "Olá Dr. Luciano! Gostaria de agendar uma consulta. Poderia me ajudar?"
  const encodedMessage = encodeURIComponent(message)
  const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodedMessage}`
  
  window.open(whatsappUrl, '_blank')
}

const openInstagram = () => {
  const instagramUrl = "https://instagram.com/luciano.tarso"
  window.open(instagramUrl, '_blank')
}
</script>

<style scoped>
.contact {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  position: relative;
  overflow: hidden;
}

.contact::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23303829' fill-opacity='0.03'%3E%3Ccircle cx='30' cy='30' r='2'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E") repeat;
  z-index: 0;
}

.container {
  position: relative;
  z-index: 1;
}

.contact__cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: var(--spacing-2xl);
  margin-bottom: var(--spacing-2xl);
}

.contact__card {
  position: relative;
  background: var(--white);
  border-radius: 24px;
  padding: var(--spacing-2xl);
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  overflow: hidden;
  border: 2px solid transparent;
  box-shadow: 0 10px 40px rgba(48, 56, 41, 0.1);
}

.contact__card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 60px rgba(48, 56, 41, 0.15);
}

.contact__card--instagram:hover {
  border-color: #e91e63;
}

.contact__card--whatsapp:hover {
  border-color: #303829;
}

.card__background {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  opacity: 0.05;
  z-index: 0;
}

.card__pattern {
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 20% 20%, #e91e63 0%, transparent 50%),
              radial-gradient(circle at 80% 80%, #f06292 0%, transparent 50%),
              radial-gradient(circle at 40% 40%, #e91e63 0%, transparent 50%);
}

.card__pattern--whatsapp {
  background: radial-gradient(circle at 20% 20%, #303829 0%, transparent 50%),
              radial-gradient(circle at 80% 80%, #1855 0%, transparent 50%),
              radial-gradient(circle at 40% 40%, #303829 0%, transparent 50%);
}

.card__content {
  position: relative;
  z-index: 1;
}

.card__header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--spacing-lg);
}

.card__icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 60px;
  height: 60px;
  border-radius: 16px;
  color: var(--white);
  flex-shrink: 0;
}

.card__icon--instagram {
  background: linear-gradient(45deg, #f09433 0%,#e6683c 25%,#dc2743 50%,#cc2366 75%,#bc1888 100%);
}

.card__icon--whatsapp {
  background-color: #303829;
}

.card__badge {
  background-color: rgba(233, 30, 99, 0.1);
  color: #e91e63;
  padding: var(--spacing-xs) var(--spacing-sm);
  border-radius: 20px;
  font-size: var(--font-size-small);
  font-weight: 600;
  border: 1px solid rgba(233, 30, 99, 0.2);
}

.card__badge--primary {
  background-color: rgba(48, 56, 41, 0.1);
  color: #303829;
  border: 1px solid rgba(48, 56, 41, 0.2);
}

.card__title {
  font-size: var(--font-size-2xl);
  font-weight: 700;
  color: #303829;
  margin-bottom: var(--spacing-md);
}

.card__description {
  color: #6c757d;
  line-height: 1.6;
  margin-bottom: var(--spacing-lg);
  font-size: var(--font-size-base);
}

.card__features {
  display: flex;
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-xl);
}

.feature__item {
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
  font-size: var(--font-size-small);
  color: #6c757d;
  font-weight: 500;
}

.feature__icon {
  font-size: var(--font-size-base);
}

.card__username {
  font-size: var(--font-size-large);
  font-weight: 700;
  color: #303829;
  background: linear-gradient(45deg, #f09433 0%,#e6683c 25%,#dc2743 50%,#cc2366 75%,#bc1888 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: var(--spacing-lg);
}

.card__phone {
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
  font-size: var(--font-size-large);
  font-weight: 600;
  color: #303829;
  margin-bottom: var(--spacing-lg);
}

.card__action {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: var(--spacing-md);
  border-top: 2px dashed rgba(48, 56, 41, 0.1);
}

.action__text {
  font-size: var(--font-size-small);
  color: #6c757d;
  font-weight: 500;
}

.action__arrow {
  width: 40px;
  height: 40px;
  background-color: #303829;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--white);
  transition: all 0.3s ease;
}

.contact__card:hover .action__arrow {
  transform: rotate(45deg);
  background-color: #d18552;
}

.contact__info {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--spacing-xl);
  background: var(--white);
  border-radius: 20px;
  padding: var(--spacing-xl);
  box-shadow: 0 5px 20px rgba(48, 56, 41, 0.08);
}

.info__item {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  padding: var(--spacing-md);
  border-radius: 12px;
  transition: all 0.3s ease;
}

.info__item:hover {
  background-color: rgba(48, 56, 41, 0.05);
}

.info__icon {
  width: 40px;
  height: 40px;
  background-color: rgba(48, 56, 41, 0.1);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #303829;
  flex-shrink: 0;
}

.info__content {
  display: flex;
  flex-direction: column;
}

.info__label {
  font-size: var(--font-size-small);
  color: #6c757d;
  font-weight: 500;
}

.info__value {
  font-size: var(--font-size-base);
  color: #303829;
  font-weight: 600;
}

/* Animações */
@keyframes float {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
}

.contact__card:nth-child(1) {
  animation: float 6s ease-in-out infinite;
}

.contact__card:nth-child(2) {
  animation: float 6s ease-in-out infinite 3s;
}

/* Responsividade */
@media (max-width: 768px) {
  .contact__cards {
    grid-template-columns: 1fr;
    gap: var(--spacing-xl);
  }
  
  .contact__card {
    padding: var(--spacing-xl);
  }
  
  .card__features {
    flex-direction: column;
    gap: var(--spacing-sm);
  }
  
  .contact__info {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
}

@media (max-width: 480px) {
  .contact__card {
    padding: var(--spacing-lg);
    border-radius: 16px;
  }
  
  .card__icon {
    width: 50px;
    height: 50px;
  }
  
  .card__icon svg {
    width: 24px;
    height: 24px;
  }
  
  .card__title {
    font-size: var(--font-size-xl);
  }
  
  .card__header {
    flex-direction: column;
    gap: var(--spacing-sm);
    align-items: flex-start;
  }
}
</style>