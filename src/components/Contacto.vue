<template>
  <section id="contacto" class="py-5 bg-primary text-white position-relative overflow-hidden w-100 d-flex justify-content-center align-items-center">
    <!-- Animated Background -->
    <div class="position-absolute top-0 start-0 w-100 h-100 overflow-hidden">
      <!-- Floating Particles -->
      <div v-for="i in 12" :key="i" 
           class="position-absolute rounded-circle bg-white bg-opacity-30 animate-float"
           :style="{
             left: Math.random() * 100 + '%',
             top: Math.random() * 100 + '%',
             animationDelay: Math.random() * 4 + 's',
             animationDuration: 3 + Math.random() * 2 + 's',
             width: '4px',
             height: '4px'
           }">
      </div>
      
      <!-- Gradient Orbs -->
      <div class="position-absolute top-0 end-0 bg-primary bg-opacity-10 rounded-circle animate-pulse-slow blur-3" 
           style="width: 256px; height: 256px; margin-top: -80px; margin-right: -80px;"></div>
      <div class="position-absolute bottom-0 start-0 bg-primary bg-opacity-10 rounded-circle animate-pulse-slower blur-3"
           style="width: 256px; height: 256px; margin-bottom: -80px; margin-left: -80px;"></div>
    </div>

    <div class="container position-relative z-3 d-flex flex-column align-items-center justify-content-center">
      <!-- Section Header -->
      <div class="text-center mb-5 w-100 d-flex flex-column align-items-center">
        <div class="d-inline-flex align-items-center bg-white bg-opacity-10 rounded-pill px-4 py-2 mb-4 border border-white border-opacity-20 justify-content-center"
             style="backdrop-filter: blur(4px);">
          <div class="bg-info rounded-circle me-2 animate-pulse" style="width: 8px; height: 8px;"></div>
          <span class="small fw-semibold text-white text-opacity-80">📞 HABLEMOS DE TU PROYECTO</span>
        </div>

        <div class="h-3 w-100"></div>
        
        <h2 class="display-4 fw-black mb-4 text-white text-center w-100">
          Comencemos Hoy
        </h2>
        <p class="h5 text-white text-opacity-80 mx-auto lead text-center">
          Contáctanos y recibe una cotización gratuita personalizada para tu proyecto. Transformemos tu idea en realidad.
        </p>
      </div>

      <div class="h-4 w-100"></div>
      
      <div class="row g-5 w-100 align-items-start">
        <!-- Contact Form -->
        <div class="col-12 col-lg-6">
          <div class="bg-white bg-opacity-10 rounded-4 p-4 border border-white border-opacity-20 shadow-lg w-100"
               style="backdrop-filter: blur(4px);">
            <h3 class="h1 fw-black text-white mb-4 text-center">Solicita Tu Cotización</h3>
            <div class="h-3 w-100"></div>
            <form class="d-flex flex-column gap-4">
              <!-- Name & Email -->
              <div class="row g-3">
                <div class="col-12 col-md-6">
                  <div class="group">
                    <label class="form-label text-white text-opacity-80 mb-2 fw-semibold text-start w-100">Nombre Completo</label>
                    <input 
                      type="text" 
                      class="form-control px-3 py-3 bg-white bg-opacity-5 border border-white border-opacity-20 rounded-3 focus-outline focus-ring focus-border text-white placeholder-white placeholder-opacity-50 transition-all duration-300 group-hover-bg text-start"
                      placeholder="Tu nombre"
                      style="border-color: rgba(255,255,255,0.2);"
                    >
                  </div>
                </div>
                <div class="col-12 col-md-6">
                  <div class="group">
                    <label class="form-label text-white text-opacity-80 mb-2 fw-semibold text-start w-100">Email</label>
                    <input 
                      type="email" 
                      class="form-control px-3 py-3 bg-white bg-opacity-5 border border-white border-opacity-20 rounded-3 focus-outline focus-ring focus-border text-white placeholder-white placeholder-opacity-50 transition-all duration-300 group-hover-bg text-start"
                      placeholder="tu@email.com"
                      style="border-color: rgba(255,255,255,0.2);"
                    >
                  </div>
                </div>
              </div>
              
              <!-- Company -->
              <div class="group">
                <label class="form-label text-white text-opacity-80 mb-2 fw-semibold text-start w-100">Empresa</label>
                <input 
                  type="text" 
                  class="form-control px-3 py-3 bg-white bg-opacity-5 border border-white border-opacity-20 rounded-3 focus-outline focus-ring focus-border text-white placeholder-white placeholder-opacity-50 transition-all duration-300 group-hover-bg text-start"
                  placeholder="Nombre de tu empresa"
                  style="border-color: rgba(255,255,255,0.2);"
                >
              </div>
              
              <!-- Service -->
              <div class="group">
                <label class="form-label text-white text-opacity-80 mb-2 fw-semibold text-start w-100">Servicio de Interés</label>
                <select class="form-select px-3 py-3 bg-white bg-opacity-5 border border-white border-opacity-20 rounded-3 focus-outline focus-ring focus-border text-white transition-all duration-300 group-hover-bg text-start"
                        style="border-color: rgba(255,255,255,0.2);">
                  <option class="bg-primary text-start">Selecciona un servicio</option>
                  <option class="bg-primary text-start">Plan Startup</option>
                  <option class="bg-primary text-start">Plan Growth</option>
                  <option class="bg-primary text-start">Plan Pro</option>
                  <option class="bg-primary text-start">Plan Enterprise</option>
                  <option class="bg-primary text-start">Desarrollo a medida</option>
                </select>
              </div>
              
              <!-- Message -->
              <div class="group">
                <label class="form-label text-white text-opacity-80 mb-2 fw-semibold text-start w-100">Mensaje</label>
                <textarea 
                  rows="5" 
                  class="form-control px-3 py-3 bg-white bg-opacity-5 border border-white border-opacity-20 rounded-3 focus-outline focus-ring focus-border text-white placeholder-white placeholder-opacity-50 transition-all duration-300 group-hover-bg resize-none text-start"
                  placeholder="Cuéntanos sobre tu proyecto, objetivos y cualquier requerimiento especial..."
                  style="border-color: rgba(255,255,255,0.2); resize: none;"
                ></textarea>
              </div>
              <div class="h-3 w-100"></div>
              <!-- Submit Button -->
              <button 
                type="submit" 
                class="btn btn-primary btn-lg w-100 fw-black py-3 rounded-3 transition-all duration-500 border-0 position-relative overflow-hidden"
              >
                <span class="position-relative z-2 d-flex align-items-center justify-content-center">
                  Enviar Solicitud
                  <span class="ms-2 transition-all duration-500 group-hover-translate">🚀</span>
                </span>
                <div class="position-absolute top-0 start-0 w-100 h-100 bg-white bg-opacity-20 skew-x-12 translate-x-n100 transition-transform duration-1000"></div>
              </button>
            </form>
          </div>
        </div>
        
        <!-- Contact Information -->
        <div class="col-12 col-lg-6">
          <div class="d-flex flex-column justify-content-center gap-4 align-items-start w-100 h-100">
            <!-- Contact Methods -->
            <div class="d-flex flex-column gap-4 w-100">
              <!-- Phone -->
              <div class="d-flex align-items-start group cursor-pointer transition-all duration-500 hover-scale w-100">
                <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center me-4 transition-all duration-500 group-hover-scale-rotate shadow"
                     style="width: 64px; height: 64px; flex-shrink: 0;">
                  <span class="fs-4">📞</span>
                </div>
                <div class="flex-grow-1 text-start">
                  <h4 class="fs-5 fw-black text-white mb-1">Teléfono</h4>
                  <p class="text-info fs-6 fw-semibold mb-1">+54 9 11 5527-1430</p>
                  <p class="text-white text-opacity-60 small">Lunes a Viernes 9:00 - 18:00</p>
                </div>
              </div>
              
              <!-- Email -->
              <div class="d-flex align-items-start group cursor-pointer transition-all duration-500 hover-scale w-100">
                <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center me-4 transition-all duration-500 group-hover-scale-rotate shadow"
                     style="width: 64px; height: 64px; flex-shrink: 0; background: linear-gradient(135deg, #0a58ca, #084298);">
                  <span class="fs-4">✉️</span>
                </div>
                <div class="flex-grow-1 text-start">
                  <h4 class="fs-5 fw-black text-white mb-1">Email</h4>
                  <p class="text-info fs-6 fw-semibold mb-1">contacto@jmgdesarrollos.com</p>
                  <p class="text-white text-opacity-60 small">Respondemos en menos de 24 horas</p>
                </div>
              </div>
              
              <!-- Location -->
              <div class="d-flex align-items-start group cursor-pointer transition-all duration-500 hover-scale w-100">
                <div class="bg-dark rounded-3 d-flex align-items-center justify-content-center me-4 transition-all duration-500 group-hover-scale-rotate shadow"
                     style="width: 64px; height: 64px; flex-shrink: 0;">
                  <span class="fs-4">📍</span>
                </div>
                <div class="flex-grow-1 text-start">
                  <h4 class="fs-5 fw-black text-white mb-1">Ubicación</h4>
                  <p class="text-info fs-6 fw-semibold mb-1">Buenos Aires, Argentina</p>
                  <p class="text-white text-opacity-60 small">Trabajamos con clientes de todo el mundo</p>
                </div>
              </div>
            </div>

            <div class="h-4 w-100"></div>
            
            <!-- Quick Contact -->
            <div class="bg-primary bg-opacity-20 rounded-4 p-4 border border-primary border-opacity-30 w-100 d-flex flex-column align-items-center text-center"
                 style="backdrop-filter: blur(4px);">
              <h4 class="h4 fw-black text-white mb-3 text-center w-100">¿Necesitas una solución urgente?</h4>
              <p class="text-white text-opacity-80 mb-3 text-center w-100">
                Contáctanos directamente por WhatsApp para una respuesta inmediata y atención personalizada.
              </p>
              <div class="h-3 w-100"></div>
              <button class="btn btn-success btn-lg w-100 fw-black py-3 rounded-3 transition-all duration-500 border-0 position-relative overflow-hidden"
                      style="max-width: 300px; background: linear-gradient(to right, #198754, #0d6efd);">
                <span class="position-relative z-2 d-flex align-items-center justify-content-center">
                  💬 Chatear por WhatsApp
                  <span class="ms-2 transition-all duration-500 group-hover-translate">→</span>
                </span>
                <div class="position-absolute top-0 start-0 w-100 h-100 bg-white bg-opacity-20 scale-x-0 transition-transform duration-500 origin-start"></div>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Lógica del componente si es necesaria
</script>

<style scoped>
/* Estilos personalizados para mantener las animaciones y efectos */

/* Animaciones */
@keyframes float {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  33% {
    transform: translateY(-20px) rotate(3deg);
  }
  66% {
    transform: translateY(-10px) rotate(-3deg);
  }
}

@keyframes pulse-slow {
  0%, 100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.8;
    transform: scale(1.05);
  }
}

@keyframes pulse-slower {
  0%, 100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.6;
    transform: scale(1.02);
  }
}

.animate-float {
  animation: float 4s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse-slow 4s ease-in-out infinite;
}

.animate-pulse-slower {
  animation: pulse-slower 6s ease-in-out infinite;
}

.animate-pulse {
  animation: pulse-slow 2s ease-in-out infinite;
}

/* Efectos blur personalizados */
.blur-3 {
  filter: blur(12px);
}

/* Efectos hover personalizados */
.group:hover .group-hover-scale-rotate {
  transform: scale(1.1) rotate(6deg);
}

.group:hover .hover-scale {
  transform: scale(1.05);
}

.group:hover .group-hover-translate {
  transform: translateX(0.5rem);
}

.group:hover .group-hover-bg {
  background-color: rgba(255, 255, 255, 0.1) !important;
}

.group:hover .scale-x-0 {
  transform: scaleX(1);
}

/* Utilidades de transición */
.transition-all {
  transition: all 0.3s ease;
}

.duration-300 {
  transition-duration: 300ms;
}

.duration-500 {
  transition-duration: 500ms;
}

/* Transform utilities */
.skew-x-12 {
  transform: skewX(-12deg);
}

.translate-x-n100 {
  transform: translateX(-100%);
}

/* Bordes redondeados personalizados */
.rounded-4 {
  border-radius: 1rem;
}

.rounded-3 {
  border-radius: 0.75rem;
}

/* Utilidades de backdrop */
.bg-opacity-10 {
  --bs-bg-opacity: 0.1;
}

.bg-opacity-20 {
  --bs-bg-opacity: 0.2;
}

.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Estilos personalizados para formularios */
.form-control, .form-select {
  border: 1px solid rgba(255, 255, 255, 0.2) !important;
  color: white !important;
  background-color: rgba(255, 255, 255, 0.05) !important;
}

.form-control::placeholder {
  color: rgba(255, 255, 255, 0.5) !important;
}

.form-control:focus, .form-select:focus {
  background-color: rgba(255, 255, 255, 0.1) !important;
  border-color: #0d6efd !important;
  box-shadow: 0 0 0 0.2rem rgba(13, 110, 253, 0.25) !important;
  color: white !important;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .display-4 {
    font-size: 2.5rem !important;
  }
  
  .h1 {
    font-size: 2rem !important;
  }
}

/* Mejoras de espaciado para móviles */
@media (max-width: 576px) {
  .py-5 {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
  
  .mb-5 {
    margin-bottom: 3rem !important;
  }
  
  .p-4 {
    padding: 1.5rem !important;
  }
}

/* Efectos de hover para botones */
.btn:hover .translate-x-n100 {
  transform: translateX(100%) skewX(-12deg) !important;
}

/* Utilidades de opacidad */
.text-opacity-80 {
  --bs-text-opacity: 0.8;
}

.text-opacity-60 {
  --bs-text-opacity: 0.6;
}

.placeholder-opacity-50::placeholder {
  opacity: 0.5;
}

/* Estilos para elementos de contacto */
.cursor-pointer {
  cursor: pointer;
}

/* Asegurar que los elementos mantengan su altura */
.h-100 {
  height: 100%;
}

.flex-grow-1 {
  flex-grow: 1;
}
</style>