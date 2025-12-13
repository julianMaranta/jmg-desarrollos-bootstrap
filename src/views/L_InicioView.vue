<script setup>
import HeaderInicio from "../components/HeaderInicio.vue";
import NuestrosServicios from "../components/NuestrosServicios.vue";
import PorqueElegirnos from "../components/PorqueElegirnos.vue";
import ProcesoDesarrollo from "../components/ProcesoDesarrollo.vue";
import TestimoniosClientes from "../components/TestimoniosClientes.vue";
import Contacto from "../components/Contacto.vue";

import { ref, onMounted, onUnmounted } from 'vue';

const isMobile = ref(false);
const isMenuOpen = ref(false);
const isScrolled = ref(false);
const activeSection = ref('inicio');

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
    activeSection.value = sectionId;
  }
  isMenuOpen.value = false;
};

const checkMobile = () => {
  isMobile.value = window.innerWidth <= 768;
};

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
  
  // Update active section based on scroll position
  const sections = ['inicio', 'servicios', 'proceso', 'testimonios', 'contacto'];
  const scrollPosition = window.scrollY + 100;
  
  for (const section of sections) {
    const element = document.getElementById(section);
    if (element) {
      const offsetTop = element.offsetTop;
      const offsetBottom = offsetTop + element.offsetHeight;
      
      if (scrollPosition >= offsetTop && scrollPosition < offsetBottom) {
        activeSection.value = section;
        break;
      }
    }
  }
};

onMounted(() => {
  checkMobile();
  window.addEventListener('resize', checkMobile);
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('resize', checkMobile);
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <div class="min-vh-100 bg-white overflow-hidden d-flex flex-column align-items-center">
    <!-- Navigation -->
    <nav 
      class="bg-white fixed-top w-100 z-50 transition-all duration-500 border-bottom border-primary-subtle d-flex justify-content-center"
      :class="isScrolled ? 'py-3 shadow-lg' : 'py-4'"
      style="backdrop-filter: blur(10px); background: rgba(255,255,255,0.95);"
    >
      <div class="container">
        <div class="d-flex justify-content-between align-items-center">
          <!-- Logo -->
          <div class="d-flex align-items-center gap-3 group cursor-pointer" @click="scrollToSection('inicio')" style="cursor: pointer;">
            <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center transition-all group-hover-scale" 
                 style="width: 48px; height: 48px; background: linear-gradient(135deg, #0d6efd, #0a58ca);">
              <span class="text-white fw-bold">JMG</span>
            </div>
            <div class="text-center">
              <span class="h5 fw-bold text-primary mb-0">JMG Desarrollos</span>
              <div class="bg-primary transition-all group-hover-line mx-auto mt-1" style="height: 2px; width: 0;"></div>
            </div>
          </div>
          
          <!-- Desktop Menu -->
          <ul class="d-none d-md-flex list-unstyled align-items-center gap-4 mb-0">
            <li 
              v-for="item in [
                { id: 'inicio', name: 'Inicio' },
                { id: 'servicios', name: 'Servicios' },
                { id: 'proceso', name: 'Proceso' },
                { id: 'testimonios', name: 'Testimonios' }
              ]" 
              :key="item.id"
              @click="scrollToSection(item.id)"
              class="cursor-pointer transition-all position-relative"
              :class="activeSection === item.id ? 'text-primary scale-110' : 'text-secondary'"
              style="cursor: pointer;"
            >
              <a class="fw-semibold position-relative z-2 px-2 py-1 text-decoration-none" 
                 :class="activeSection === item.id ? 'text-primary' : 'text-secondary'">
                {{ item.name }}
              </a>
              <div 
                class="position-absolute bottom-0 start-50 translate-middle-x bg-primary rounded-pill transition-all"
                :class="activeSection === item.id ? 'w-100' : 'w-0'"
                style="height: 2px; background: linear-gradient(to right, #0d6efd, #0a58ca);"
              ></div>
            </li>
            <li 
              @click="scrollToSection('contacto')" 
              class="cursor-pointer bg-primary text-white px-4 py-2 rounded-3 transition-all fw-semibold shadow position-relative overflow-hidden"
              style="background: linear-gradient(to right, #0d6efd, #0a58ca); cursor: pointer;"
            >
              <span class="position-relative z-2">Contacto</span>
            </li>
          </ul>

          <!-- Mobile Menu Button -->
          <button 
            @click="toggleMenu" 
            class="d-md-none btn btn-primary p-2 position-relative z-5 border-0"
            style="background: linear-gradient(135deg, #0d6efd, #0a58ca); width: 40px; height: 40px;"
            aria-label="Menú"
          >
            <span class="d-block w-75 h-1 bg-white mb-1 rounded transition-all position-absolute top-25 start-50 translate-middle" 
                  :class="{ 'rotate-45 top-50': isMenuOpen }"></span>
            <span class="d-block w-75 h-1 bg-white mb-1 rounded transition-all position-absolute top-50 start-50 translate-middle" 
                  :class="{ 'opacity-0': isMenuOpen }"></span>
            <span class="d-block w-75 h-1 bg-white rounded transition-all position-absolute bottom-25 start-50 translate-middle" 
                  :class="{ 'rotate-[-45deg] top-50': isMenuOpen }"></span>
          </button>
        </div>

        <!-- Mobile Menu -->
        <div 
          v-if="isMobile && isMenuOpen" 
          class="d-md-none bg-white border-top border-primary-subtle py-4 rounded-bottom-3 shadow-lg mt-2 text-center"
          style="backdrop-filter: blur(10px);"
        >
          <ul class="list-unstyled mb-0">
            <li 
              v-for="item in [
                { id: 'inicio', name: 'Inicio' },
                { id: 'servicios', name: 'Servicios' },
                { id: 'proceso', name: 'Proceso' },
                { id: 'testimonios', name: 'Testimonios' }
              ]" 
              :key="item.id"
              @click="scrollToSection(item.id)"
              class="cursor-pointer transition-all py-3 px-4 rounded-3 mx-2"
              :class="activeSection === item.id ? 'bg-primary bg-opacity-10 text-primary' : 'text-secondary'"
              style="cursor: pointer;"
            >
              <a class="fw-semibold d-flex align-items-center justify-content-center text-decoration-none"
                 :class="activeSection === item.id ? 'text-primary' : 'text-secondary'">
                <div class="bg-primary rounded-circle me-3 transition-all" 
                     :class="activeSection === item.id ? 'scale-100' : 'scale-0'"
                     style="width: 8px; height: 8px;"></div>
                {{ item.name }}
              </a>
            </li>
            <li 
              @click="scrollToSection('contacto')" 
              class="cursor-pointer bg-primary text-white px-4 py-3 rounded-3 transition-all fw-semibold shadow mt-3 mx-2 text-center border-0"
              style="background: linear-gradient(to right, #0d6efd, #0a58ca); cursor: pointer;"
            >
              <a class="text-white text-decoration-none">Contacto</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="pt-5 w-100 d-flex flex-column align-items-center">
      <HeaderInicio />
      <NuestrosServicios />
      <PorqueElegirnos />
      <ProcesoDesarrollo />
      <TestimoniosClientes />
      <Contacto />
    </main>

    <!-- Floating Action Buttons -->
    <div class="fixed-bottom end-0 p-3 z-40 d-flex flex-column gap-3">
      <!-- WhatsApp Button -->
      <button 
        class="btn btn-success rounded-3 shadow-lg d-flex align-items-center justify-content-center transition-all"
        style="width: 64px; height: 64px;"
        aria-label="WhatsApp"
      >
        <span class="fs-5">💬</span>
      </button>
      
      <!-- Scroll to Top -->
      <button 
        @click="scrollToSection('inicio')"
        class="btn btn-primary rounded-3 shadow-lg d-flex align-items-center justify-content-center transition-all border-0"
        style="width: 64px; height: 64px; background: linear-gradient(135deg, #0d6efd, #0a58ca);"
        aria-label="Volver arriba"
      >
        <span class="fs-5">↑</span>
      </button>
    </div>

    <!-- Footer -->
    <footer class="bg-dark text-white py-5 w-100 position-relative overflow-hidden">
      <!-- Background Elements -->
      <div class="position-absolute top-0 start-0 w-100 h-100 overflow-hidden">
        <div class="position-absolute bg-primary bg-opacity-10 rounded-circle" 
             style="width: 160px; height: 160px; top: -80px; right: -80px;"></div>
        <div class="position-absolute bg-primary bg-opacity-10 rounded-circle" 
             style="width: 160px; height: 160px; bottom: -80px; left: -80px;"></div>
        <div class="position-absolute top-50 start-25 bg-primary bg-opacity-20 rounded-circle animate-float"
             style="width: 32px; height: 32px;"></div>
        <div class="position-absolute bottom-33 end-25 bg-primary bg-opacity-20 rounded-circle animate-float-delayed"
             style="width: 24px; height: 24px;"></div>
      </div>
      
      <div class="container position-relative z-2">
        <div class="row g-4 text-center text-md-start">
          <!-- Logo y Descripción -->
          <div class="col-12 col-md-3 d-flex flex-column align-items-center align-items-md-start">
            <div class="d-flex align-items-center gap-3 justify-content-center justify-content-md-start mb-3 group cursor-pointer" @click="scrollToSection('inicio')" style="cursor: pointer;">
              <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center"
                   style="width: 56px; height: 56px; background: linear-gradient(135deg, #0d6efd, #0a58ca);">
                <span class="text-white fw-bold">JMG</span>
              </div>
              <span class="h4 fw-bold text-info mb-0">JMG Desarrollos</span>
            </div>
            <p class="text-secondary mb-3 text-center text-md-start">
              Creamos soluciones web innovadoras que impulsan el crecimiento de tu negocio con tecnología de vanguardia.
            </p>
            <p class="text-secondary-emphasis small text-center text-md-start">&copy; 2024 JMG Desarrollos. Todos los derechos reservados.</p>
          </div>
          
          <!-- Enlaces rápidos -->
          <div class="col-12 col-md-3 d-flex flex-column align-items-center align-items-md-start">
            <h3 class="h5 fw-bold mb-3 text-info">Enlaces Rápidos</h3>
            <ul class="list-unstyled">
              <li v-for="link in ['inicio', 'servicios', 'proceso', 'testimonios']" :key="link" class="mb-2">
                <a 
                  @click="scrollToSection(link)" 
                  class="text-secondary text-decoration-none transition-all d-flex align-items-center justify-content-center justify-content-md-start"
                  style="cursor: pointer;"
                >
                  <div class="bg-info rounded-circle me-2 opacity-0 transition-all group-hover-opacity" style="width: 4px; height: 4px;"></div>
                  {{ link.charAt(0).toUpperCase() + link.slice(1) }}
                </a>
              </li>
            </ul>
          </div>
          
          <!-- Contacto -->
          <div class="col-12 col-md-3 d-flex flex-column align-items-center align-items-md-start">
            <h3 class="h5 fw-bold mb-3 text-info">Contacto</h3>
            <div class="d-flex flex-column gap-3 text-secondary align-items-center align-items-md-start">
              <p class="d-flex align-items-center transition-all mb-0 justify-content-center justify-content-md-start group">
                <span class="bg-primary rounded-circle d-flex align-items-center justify-content-center me-3 text-white transition-all group-hover-scale"
                      style="width: 32px; height: 32px; background: linear-gradient(135deg, #0d6efd, #0a58ca);">📞</span>
                +54 9 11 5527-1430
              </p>
              <p class="d-flex align-items-center transition-all mb-0 justify-content-center justify-content-md-start group">
                <span class="bg-primary rounded-circle d-flex align-items-center justify-content-center me-3 text-white transition-all group-hover-scale"
                      style="width: 32px; height: 32px; background: linear-gradient(135deg, #0d6efd, #0a58ca);">✉️</span>
                contacto@jmgdesarrollos.com
              </p>
              <p class="d-flex align-items-center transition-all mb-0 justify-content-center justify-content-md-start group">
                <span class="bg-primary rounded-circle d-flex align-items-center justify-content-center me-3 text-white transition-all group-hover-scale"
                      style="width: 32px; height: 32px; background: linear-gradient(135deg, #0d6efd, #0a58ca);">📍</span>
                Buenos Aires, Argentina
              </p>
            </div>
          </div>
          
          <!-- Redes sociales -->
          <div class="col-12 col-md-3 d-flex flex-column align-items-center align-items-md-start">
            <h3 class="h5 fw-bold mb-3 text-info">Síguenos</h3>
            <div class="d-flex justify-content-center justify-content-md-start gap-2">
              <a 
                v-for="(social, index) in [
                  { name: 'FB', icon: '📘', color: 'btn-primary' },
                  { name: 'IG', icon: '📷', color: 'btn-primary' },
                  { name: 'IN', icon: '💼', color: 'btn-primary' },
                  { name: 'WA', icon: '💚', color: 'btn-primary' }
                ]" 
                :key="social.name" 
                href="#" 
                class="btn rounded-2 d-flex align-items-center justify-content-center transition-all border-0"
                :class="social.color"
                style="width: 48px; height: 48px;"
              >
                <span class="text-white">{{ social.icon }}</span>
              </a>
            </div>
          </div>
        </div>
        
        <!-- Divider -->
        <div class="border-top border-primary border-opacity-50 mt-4 pt-4 text-center">
          <p class="text-secondary-emphasis small mb-0">
            Hecho con ❤️ por JMG Desarrollos - Transformando ideas en realidad digital
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* Estilos personalizados para mantener las animaciones y efectos */
.min-vh-100 {
  min-height: 100vh;
}

.group:hover .group-hover-scale {
  transform: scale(1.1) rotate(6deg);
}

.group:hover .group-hover-line {
  width: 100% !important;
}

.group:hover .group-hover-scale {
  transform: scale(1.1);
}

.group:hover .group-hover-opacity {
  opacity: 1 !important;
}

.scale-110 {
  transform: scale(1.1);
}

.scale-0 {
  transform: scale(0);
}

.scale-100 {
  transform: scale(1);
}

.rotate-45 {
  transform: rotate(45deg);
}



.transition-all {
  transition: all 0.3s ease;
}

.cursor-pointer {
  cursor: pointer;
}

/* Posicionamiento utilities */
.top-25 {
  top: 25%;
}

.top-50 {
  top: 50%;
}

.bottom-25 {
  bottom: 25%;
}

.bottom-33 {
  bottom: 33%;
}

.start-25 {
  left: 25%;
}

.start-50 {
  left: 50%;
}

.end-25 {
  right: 25%;
}

.translate-middle {
  transform: translate(-50%, -50%);
}

.translate-middle-x {
  transform: translateX(-50%);
}

.z-40 {
  z-index: 40;
}

.z-50 {
  z-index: 50;
}

/* Animaciones personalizadas */
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

@keyframes float-delayed {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  33% {
    transform: translateY(-15px) rotate(-2deg);
  }
  66% {
    transform: translateY(-8px) rotate(2deg);
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

.animate-float-delayed {
  animation: float-delayed 5s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse-slow 4s ease-in-out infinite;
}

.animate-pulse-slower {
  animation: pulse-slower 6s ease-in-out infinite;
}

/* Background opacity utilities */
.bg-opacity-10 {
  --bs-bg-opacity: 0.1;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .pt-5 {
    padding-top: 4rem !important;
  }
}

/* Hover effects for footer links */
.group:hover {
  transform: translateX(0.5rem);
}
</style>