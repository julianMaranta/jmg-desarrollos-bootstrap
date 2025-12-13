<template>
  <header id="inicio" class="min-vh-80 bg-primary text-white position-relative overflow-hidden d-flex align-items-center justify-content-center w-100">
    <!-- Animated Background -->
    <div class="position-absolute top-0 start-0 w-100 h-100 overflow-hidden">
      <!-- Floating Particles -->
      <div v-for="i in 10" :key="i" 
           class="position-absolute rounded-circle bg-white bg-opacity-10 animate-float"
           :style="{
             left: Math.random() * 100 + '%',
             top: Math.random() * 100 + '%',
             animationDelay: Math.random() * 5 + 's',
             animationDuration: 3 + Math.random() * 2 + 's',
             width: '6px',
             height: '6px'
           }">
      </div>
      
      <!-- Gradient Orbs -->
      <div class="position-absolute top-0 end-0 bg-primary bg-opacity-20 rounded-circle animate-pulse-slow blur-3" 
           style="width: 200px; height: 200px; margin-top: -80px; margin-right: -80px;"></div>
      <div class="position-absolute bottom-0 start-0 bg-primary bg-opacity-20 rounded-circle animate-pulse-slower blur-3"
           style="width: 200px; height: 200px; margin-bottom: -80px; margin-left: -80px;"></div>
    </div>
    
    <div class="w-100 text-center position-relative z-3 py-5 d-flex flex-column align-items-center px-3">
      <!-- Main Content -->
      <div class="animate-fade-in-up w-100 d-flex flex-column align-items-center" style="max-width: 1200px;">
        <!-- Badge - CARTEL 100% VISIBLE -->
        <div class="d-inline-flex align-items-center bg-white bg-opacity-10 rounded-pill px-4 py-3 mb-4 border border-white border-opacity-20 animate-pulse"
             style="backdrop-filter: blur(4px); margin-top: 2rem;">
          <div class="bg-info rounded-circle me-3 animate-ping" style="width: 10px; height: 10px; flex-shrink: 0;"></div>
          <span class="fw-semibold text-white text-opacity-80" style="font-size: 0.9rem;">🚀 Listos para impulsar tu negocio</span>
        </div>

        <!-- Main Heading -->
        <h1 class="display-4 fw-black mb-4 text-center w-100 text-white">
          <span class="d-block animate-slide-in-left mb-2">
            Impulsa Tu
          </span>
          <span class="d-block animate-slide-in-right delay-300">
            Negocio Digital
          </span>
        </h1>

        <!-- Subheading -->
        <p class="h6 mb-4 text-white text-opacity-80 mx-auto text-center w-100 animate-fade-in-up delay-500 px-2"
           style="max-width: 700px;">
          Creamos <span class="text-info fw-semibold">experiencias web extraordinarias</span> que convierten visitantes en clientes leales
        </p>

        <!-- CTA Buttons -->
        <div class="d-flex flex-column flex-sm-row gap-3 justify-content-center align-items-center py-3 my-3 animate-fade-in-up delay-700 w-100">
          <button 
            @click="scrollToSection('servicios')"
            class="btn btn-primary btn-lg position-relative overflow-hidden border-0 fw-bold px-4 py-2 rounded-3 transition-all"
            style="background: linear-gradient(to right, #0d6efd, #0a58ca); min-width: 200px;"
          >
            <span class="position-relative z-2 d-flex align-items-center justify-content-center text-white">
              Explorar Servicios
              <i class="bi bi-arrow-right ms-2 transition-all btn-arrow"></i>
            </span>
            <div class="position-absolute top-0 start-0 w-100 h-100 bg-white bg-opacity-20 skew-x-12 translate-x-n100 transition-transform duration-1000"></div>
          </button>
          
          <button 
            @click="scrollToSection('contacto')"
            class="btn btn-outline-light btn-lg position-relative overflow-hidden fw-bold px-4 py-2 rounded-3 transition-all"
            style="min-width: 200px; border-width: 2px; background: transparent;"
          >
            <span class="position-relative z-2 d-flex align-items-center justify-content-center text-white">
              <i class="bi bi-chat me-2"></i>
              Contactar Ahora
            </span>
            <div class="position-absolute top-0 start-0 w-100 h-100 bg-white bg-opacity-10 scale-0 rounded-3 transition-transform duration-500"></div>
          </button>
        </div>

        <!-- Stats -->
        <div class="row g-3 mx-auto animate-fade-in-up delay-1000 w-100 mt-4 justify-content-center"
             style="max-width: 900px;">
          <div v-for="(stat, index) in stats" :key="index" 
               class="col-6 col-lg-3 text-center transition-all duration-500 group">
            <div class="position-relative">
              <div class="fs-1 fw-black text-white mb-2 animate-count-up" 
                   :data-target="stat.value"
                   style="text-shadow: 0 2px 4px rgba(0,0,0,0.3);">
                {{ stat.value }}+
              </div>
            </div>
            <div class="text-white text-opacity-80 small fw-semibold text-uppercase">{{ stat.label }}</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Floating Elements Minimizados -->
    <div class="position-absolute top-25 start-15 bg-primary bg-opacity-20 rounded-circle animate-float-delayed" style="width: 8px; height: 8px;"></div>
    <div class="position-absolute top-40 end-20 bg-primary bg-opacity-20 rounded-circle animate-float" style="width: 6px; height: 6px;"></div>
  </header>
</template>

<script setup>
const stats = [
  { 
    value: 200, 
    label: 'Proyectos Entregados'
  },
  { 
    value: 98, 
    label: 'Clientes Satisfechos'
  },
  { 
    value: 24, 
    label: 'Soporte Técnico'
  },
  { 
    value: 5, 
    label: 'Años de Experiencia'
  }
];

const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};

// Counter animation
import { onMounted } from 'vue';

onMounted(() => {
  const counters = document.querySelectorAll('.animate-count-up');
  
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const counter = entry.target;
        const target = parseInt(counter.getAttribute('data-target'));
        const duration = 2000;
        const step = target / (duration / 16);
        let current = 0;
        
        const timer = setInterval(() => {
          current += step;
          if (current >= target) {
            counter.textContent = target + '+';
            clearInterval(timer);
          } else {
            counter.textContent = Math.floor(current) + '+';
          }
        }, 16);
        
        observer.unobserve(counter);
      }
    });
  }, { threshold: 0.5 });
  
  counters.forEach(counter => observer.observe(counter));
});
</script>

<style scoped>
/* Altura aumentada para evitar cortes */
.min-vh-80 {
  min-height: 80vh;
}

/* Posicionamiento utilities */
.top-25 {
  top: 25%;
}

.top-40 {
  top: 40%;
}

.start-15 {
  left: 15%;
}

.end-20 {
  right: 20%;
}

.blur-3 {
  filter: blur(12px);
}

.skew-x-12 {
  transform: skewX(-12deg);
}

.translate-x-n100 {
  transform: translateX(-100%);
}

/* CORRECCIÓN DEFINITIVA: Cartel 100% visible */
.rounded-pill {
  margin-top: 2rem !important;
  padding: 0.75rem 1.5rem !important;
}

/* Animaciones personalizadas */
@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(20px) scale(0.98);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes slide-in-left {
  from {
    opacity: 0;
    transform: translateX(-40px) rotate(-2deg);
  }
  to {
    opacity: 1;
    transform: translateX(0) rotate(0);
  }
}

@keyframes slide-in-right {
  from {
    opacity: 0;
    transform: translateX(40px) rotate(2deg);
  }
  to {
    opacity: 1;
    transform: translateX(0) rotate(0);
  }
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  33% {
    transform: translateY(-10px) rotate(1deg);
  }
  66% {
    transform: translateY(-5px) rotate(-1deg);
  }
}

@keyframes float-delayed {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  33% {
    transform: translateY(-8px) rotate(-1deg);
  }
  66% {
    transform: translateY(-4px) rotate(1deg);
  }
}

@keyframes pulse-slow {
  0%, 100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.8;
    transform: scale(1.02);
  }
}

@keyframes pulse-slower {
  0%, 100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.6;
    transform: scale(1.01);
  }
}

@keyframes ping {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  75%, 100% {
    transform: scale(1.3);
    opacity: 0;
  }
}

.animate-fade-in-up {
  animation: fade-in-up 0.5s ease-out;
}

.animate-slide-in-left {
  animation: slide-in-left 0.4s ease-out;
}

.animate-slide-in-right {
  animation: slide-in-right 0.4s ease-out;
}

.animate-float {
  animation: float 2.5s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float-delayed 3s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse-slow 2.5s ease-in-out infinite;
}

.animate-pulse-slower {
  animation: pulse-slower 4s ease-in-out infinite;
}

.animate-ping {
  animation: ping 1.2s ease-in-out infinite;
}

.delay-300 {
  animation-delay: 300ms;
}

.delay-500 {
  animation-delay: 500ms;
}

.delay-700 {
  animation-delay: 700ms;
}

.delay-1000 {
  animation-delay: 1000ms;
}

/* Hover effects */
.btn:hover .btn-arrow {
  transform: translateX(3px);
}

.btn:hover .scale-0 {
  transform: scale(1) !important;
}

.btn:hover .translate-x-n100 {
  transform: translateX(100%) skewX(-12deg) !important;
}

.transition-all {
  transition: all 0.3s ease;
}

/* CORRECCIÓN: Botón Contactar Ahora VISIBLE */
.btn-outline-light {
  color: white !important;
  border-color: rgba(255, 255, 255, 0.6) !important;
  background-color: transparent !important;
}

.btn-outline-light:hover {
  color: #000 !important;
  background-color: rgba(255, 255, 255, 0.95) !important;
  border-color: white !important;
}

.btn-outline-light .text-white {
  color: white !important;
}

.btn-outline-light:hover .text-white {
  color: #000 !important;
}

/* CORRECCIÓN DEFINITIVA: Cartel 100% visible en todos los dispositivos */
@media (max-width: 768px) {
  .min-vh-80 {
    min-height: 85vh;
  }
  
  .rounded-pill {
    margin-top: 1.5rem !important;
    padding: 0.6rem 1.2rem !important;
    white-space: normal !important;
    text-align: center;
    max-width: 300px;
  }
  
  .display-4 {
    font-size: 2.2rem !important;
  }
  
  .fs-1 {
    font-size: 1.75rem !important;
  }
  
  .h6 {
    font-size: 1rem !important;
  }
  
  .btn-lg {
    padding: 0.7rem 1.2rem !important;
    font-size: 0.9rem !important;
    min-width: 180px !important;
  }
  
  .py-5 {
    padding-top: 2rem !important;
    padding-bottom: 2rem !important;
  }
}

@media (max-width: 576px) {
  .min-vh-80 {
    min-height: 90vh;
  }
  
  .rounded-pill {
    margin-top: 1rem !important;
    padding: 0.5rem 1rem !important;
    max-width: 280px;
  }
  
  .rounded-pill span {
    font-size: 0.8rem !important;
    line-height: 1.3;
  }
  
  .display-4 {
    font-size: 1.8rem !important;
  }
  
  .fs-1 {
    font-size: 1.5rem !important;
  }
  
  .py-5 {
    padding-top: 1.5rem !important;
    padding-bottom: 1.5rem !important;
  }
}

@media (min-width: 1200px) {
  .min-vh-80 {
    min-height: 75vh;
  }
  
  .rounded-pill {
    margin-top: 2.5rem !important;
  }
}

/* Utilidades de opacidad */
.text-opacity-80 {
  --bs-text-opacity: 0.8;
}

/* Background opacity utilities */
.bg-opacity-10 {
  --bs-bg-opacity: 0.1;
}

.bg-opacity-20 {
  --bs-bg-opacity: 0.2;
}

/* Backdrop blur */
.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Espaciado seguro */
.py-5 {
  padding-top: 3rem !important;
  padding-bottom: 3rem !important;
}

.mb-4 {
  margin-bottom: 1.5rem !important;
}

.py-3 {
  padding-top: 1rem !important;
  padding-bottom: 1rem !important;
}

.mt-4 {
  margin-top: 1.5rem !important;
}

/* Garantizar que el cartel tenga suficiente espacio */
header {
  overflow: visible !important;
}
</style>