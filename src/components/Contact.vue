<template>
  <section id="contato" class="contact section">
    <div class="container">
      <h2 class="section-title">Entre em Contacto</h2>
      <p class="section-subtitle">
        Pronto para dar o primeiro passo? Entre em contacto para marcar a sua consulta
      </p>
      
      <div class="contact__content">
        <div class="contact__info">
          <h3 class="contact__info-title">Informações de Contacto</h3>
          
          
          <div class="contact__item">
            <div class="contact__item-icon">📞</div>
            <div class="contact__item-content">
              <h4>Telefone</h4>
              <p> 34 99687-7462</p>
            </div>
          </div>
          
          <div class="contact__item">
            <div class="contact__item-icon">✉️</div>
            <div class="contact__item-content">
              <h4>Email</h4>
              <p>tarsoluciano@gmail.com</p>
            </div>
          </div>

          <div class="contact__item">
            <div class="contact__item-icon">📱</div>
            <div class="contact__item-content">
              <h4>Instagram</h4>
              <p>@luciano.tarso</p>
            </div>
         </div>
          
          <div class="contact__item">
            <div class="contact__item-icon">🕒</div>
            <div class="contact__item-content">
              <h4>Horário de Atendimento</h4>
              <p>Segunda a Sexta: 9h00 - 19h00<br>Sábado: 9h00 - 13h00</p>
            </div>
          </div>
          
        </div>
        
        <div class="contact__form">
          <h3 class="contact__form-title">Marcar Consulta</h3>
          <form @submit.prevent="submitForm" class="form">
            <div class="form__group">
              <label for="name" class="form__label">Nome Completo *</label>
              <input 
                type="text" 
                id="name" 
                v-model="form.name" 
                class="form__input"
                :class="{ 'form__input--error': errors.name }"
                required
              >
              <span v-if="errors.name" class="form__error">{{ errors.name }}</span>
            </div>
            
            <div class="form__row">
              <div class="form__group">
                <label for="email" class="form__label">Email *</label>
                <input 
                  type="email" 
                  id="email" 
                  v-model="form.email" 
                  class="form__input"
                  :class="{ 'form__input--error': errors.email }"
                  required
                >
                <span v-if="errors.email" class="form__error">{{ errors.email }}</span>
              </div>
              
              <div class="form__group">
                <label for="phone" class="form__label">Telefone</label>
                <input 
                  type="tel" 
                  id="phone" 
                  v-model="form.phone" 
                  class="form__input"
                >
              </div>
            </div>
            
            <div class="form__group">
              <label for="service" class="form__label">Tipo de Serviço *</label>
              <select 
                id="service" 
                v-model="form.service" 
                class="form__select"
                :class="{ 'form__input--error': errors.service }"
                required
              >
                <option value="">Selecione um serviço</option>
                <option value="individual">Terapia Individual</option>
                <option value="casal">Terapia de Casal</option>
                <option value="familiar">Terapia Familiar</option>
                <option value="stress">Gestão do Stress</option>
                <option value="vocacional">Orientação Vocacional</option>
                <option value="organizacional">Psicologia Organizacional</option>
              </select>
              <span v-if="errors.service" class="form__error">{{ errors.service }}</span>
            </div>
            
            <div class="form__row">
              <div class="form__group">
                <label for="modality" class="form__label">Modalidade *</label>
                <select 
                  id="modality" 
                  v-model="form.modality" 
                  class="form__select"
                  :class="{ 'form__input--error': errors.modality }"
                  required
                >
                  <option value="">Selecione a modalidade</option>
                  <option value="presencial">Presencial</option>
                  <option value="online">Online</option>
                  <option value="hibrida">Híbrida</option>
                </select>
                <span v-if="errors.modality" class="form__error">{{ errors.modality }}</span>
              </div>
              
              <div class="form__group">
                <label for="preferred-time" class="form__label">Horário Preferencial</label>
                <select id="preferred-time" v-model="form.preferredTime" class="form__select">
                  <option value="">Selecione o horário</option>
                  <option value="manha">Manhã (9h-12h)</option>
                  <option value="tarde">Tarde (14h-17h)</option>
                  <option value="final-tarde">Final de Tarde (17h-19h)</option>
                  <option value="sabado">Sábado de Manhã</option>
                </select>
              </div>
            </div>
            
            <div class="form__group">
              <label for="message" class="form__label">Mensagem</label>
              <textarea 
                id="message" 
                v-model="form.message" 
                class="form__textarea"
                rows="4"
                placeholder="Descreva brevemente o motivo da consulta ou questões que gostaria de abordar..."
              ></textarea>
            </div>
            
            <div class="form__group">
              <label class="form__checkbox">
                <input 
                  type="checkbox" 
                  v-model="form.privacy" 
                  :class="{ 'form__input--error': errors.privacy }"
                  required
                >
                <span class="form__checkbox-text">
                  Concordo com a <a href="#" class="form__link">Política de Privacidade</a> 
                  e autorizo o tratamento dos meus dados pessoais *
                </span>
              </label>
              <span v-if="errors.privacy" class="form__error">{{ errors.privacy }}</span>
            </div>
            
            <button 
              type="submit" 
              class="btn btn-primary form__submit"
              :disabled="isSubmitting"
            >
              {{ isSubmitting ? 'A Enviar...' : 'Enviar Pedido' }}
            </button>
          </form>
          
          <div v-if="submitMessage" class="form__message" :class="submitMessageClass">
            {{ submitMessage }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  phone: '',
  service: '',
  modality: '',
  preferredTime: '',
  message: '',
  privacy: false
})

const errors = ref({})
const isSubmitting = ref(false)
const submitMessage = ref('')
const submitMessageClass = ref('')

const validateForm = () => {
  errors.value = {}
  
  if (!form.name.trim()) {
    errors.value.name = 'Nome é obrigatório'
  }
  
  if (!form.email.trim()) {
    errors.value.email = 'Email é obrigatório'
  } else if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(form.email)) {
    errors.value.email = 'Email inválido'
  }
  
  if (!form.service) {
    errors.value.service = 'Selecione um serviço'
  }
  
  if (!form.modality) {
    errors.value.modality = 'Selecione uma modalidade'
  }
  
  if (!form.privacy) {
    errors.value.privacy = 'Deve concordar com a política de privacidade'
  }
  
  return Object.keys(errors.value).length === 0
}

const submitForm = async () => {
  if (!validateForm()) {
    return
  }
  
  isSubmitting.value = true
  
  try {
    // Simular envio do formulário
    await new Promise(resolve => setTimeout(resolve, 2000))
    
    submitMessage.value = 'Pedido enviado com sucesso! Entrarei em contacto consigo em breve.'
    submitMessageClass.value = 'form__message--success'
    
    // Limpar formulário
    Object.keys(form).forEach(key => {
      if (typeof form[key] === 'boolean') {
        form[key] = false
      } else {
        form[key] = ''
      }
    })
    
  } catch (error) {
    submitMessage.value = 'Erro ao enviar pedido. Tente novamente ou contacte diretamente.'
    submitMessageClass.value = 'form__message--error'
  } finally {
    isSubmitting.value = false
    
    // Limpar mensagem após 5 segundos
    setTimeout(() => {
      submitMessage.value = ''
    }, 5000)
  }
}
</script>

<style scoped>
.contact {
  background-color: var(--light-gray);
}

.contact__content {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: var(--spacing-2xl);
  align-items: start;
}

.contact__info {
  background-color: var(--white);
  border-radius: 16px;
  padding: var(--spacing-xl);
  box-shadow: var(--shadow-sm);
}

.contact__info-title {
  font-size: var(--font-size-xl);
  font-weight: 600;
  color: var(--primary-color);
  margin-bottom: var(--spacing-lg);
}

.contact__item {
  display: flex;
  align-items: flex-start;
  gap: var(--spacing-md);
  margin-bottom: var(--spacing-lg);
  padding-bottom: var(--spacing-lg);
  border-bottom: 1px solid rgba(48, 56, 41, 0.1);
}

.contact__item:last-of-type {
  border-bottom: none;
  margin-bottom: var(--spacing-xl);
}

.contact__item-icon {
  font-size: var(--font-size-xl);
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--light-gray);
  border-radius: 50%;
  flex-shrink: 0;
}

.contact__item-content h4 {
  font-size: var(--font-size-base);
  font-weight: 600;
  color: var(--primary-color);
  margin: 0 0 var(--spacing-xs) 0;
}

.contact__item-content p {
  color: var(--neutral-color);
  margin: 0;
  line-height: 1.5;
}

.contact__emergency {
  background-color: #fff3cd;
  border: 1px solid #ffeaa7;
  border-radius: 8px;
  padding: var(--spacing-md);
}

.contact__emergency-title {
  font-size: var(--font-size-base);
  font-weight: 600;
  color: #856404;
  margin: 0 0 var(--spacing-xs) 0;
}

.contact__emergency-text {
  color: #856404;
  margin: 0 0 var(--spacing-sm) 0;
  font-size: var(--font-size-small);
}

.contact__emergency-numbers {
  font-size: var(--font-size-small);
  color: #856404;
  font-weight: 500;
}

.contact__emergency-numbers div {
  margin-bottom: 2px;
}

.contact__form {
  background-color: var(--white);
  border-radius: 16px;
  padding: var(--spacing-xl);
  box-shadow: var(--shadow-sm);
}

.contact__form-title {
  font-size: var(--font-size-xl);
  font-weight: 600;
  color: var(--primary-color);
  margin-bottom: var(--spacing-lg);
}

.form__group {
  margin-bottom: var(--spacing-md);
}

.form__row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--spacing-md);
}

.form__label {
  display: block;
  font-weight: 500;
  color: var(--primary-color);
  margin-bottom: var(--spacing-xs);
  font-size: var(--font-size-small);
}

.form__input,
.form__select,
.form__textarea {
  width: 100%;
  padding: var(--spacing-sm);
  border: 1px solid rgba(48, 56, 41, 0.2);
  border-radius: 8px;
  font-size: var(--font-size-base);
  transition: border-color var(--transition-fast);
}

.form__input:focus,
.form__select:focus,
.form__textarea:focus {
  outline: none;
  border-color: var(--accent-color);
  box-shadow: 0 0 0 3px rgba(209, 133, 82, 0.1);
}

.form__input--error {
  border-color: #dc3545;
}

.form__error {
  display: block;
  color: #dc3545;
  font-size: var(--font-size-small);
  margin-top: var(--spacing-xs);
}

.form__checkbox {
  display: flex;
  align-items: flex-start;
  gap: var(--spacing-sm);
  cursor: pointer;
}

.form__checkbox input[type="checkbox"] {
  margin: 0;
  flex-shrink: 0;
  margin-top: 2px;
}

.form__checkbox-text {
  font-size: var(--font-size-small);
  color: var(--neutral-color);
  line-height: 1.4;
}

.form__link {
  color: var(--accent-color);
  text-decoration: none;
}

.form__link:hover {
  text-decoration: underline;
}

.form__submit {
  width: 100%;
  padding: var(--spacing-md);
  font-size: var(--font-size-base);
  margin-top: var(--spacing-md);
}

.form__submit:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}

.form__message {
  margin-top: var(--spacing-md);
  padding: var(--spacing-sm);
  border-radius: 8px;
  font-size: var(--font-size-small);
  text-align: center;
}

.form__message--success {
  background-color: #d4edda;
  color: #155724;
  border: 1px solid #c3e6cb;
}

.form__message--error {
  background-color: #f8d7da;
  color: #721c24;
  border: 1px solid #f5c6cb;
}

/* Responsividade */
@media (max-width: 1024px) {
  .contact__content {
    grid-template-columns: 1fr;
    gap: var(--spacing-xl);
  }
}

@media (max-width: 768px) {
  .contact__info,
  .contact__form {
    padding: var(--spacing-lg);
  }
  
  .form__row {
    grid-template-columns: 1fr;
    gap: 0;
  }
}

@media (max-width: 480px) {
  .contact__item {
    flex-direction: column;
    text-align: center;
  }
  
  .contact__info-title,
  .contact__form-title {
    font-size: var(--font-size-large);
  }
}
</style>

