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
  <div class="min-h-screen bg-white overflow-hidden flex flex-col items-center">
    <!-- Navigation -->
    <nav 
      class="bg-white/95 backdrop-blur-xl text-gray-800 fixed w-full top-0 z-50 transition-all duration-500 border-b border-blue-200/50 flex justify-center"
      :class="isScrolled ? 'py-3 shadow-2xl' : 'py-5'"
    >
      <div class="w-full max-w-7xl mx-auto px-6">
        <div class="flex justify-between items-center">
          <!-- Logo - Más separación entre logo y texto -->
          <div class="flex items-center space-x-6 group cursor-pointer" @click="scrollToSection('inicio')">
            <div class="w-12 h-12 bg-gradient-to-br from-blue-600 to-blue-800 rounded-xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
              <span class="text-white font-bold text-lg">JMG</span>
            </div>
            <div class="text-center">
              <span class="text-xl font-bold bg-gradient-to-r from-blue-600 to-blue-800 bg-clip-text text-transparent">JMG Desarrollos</span>
              <div class="h-1 w-0 bg-gradient-to-r from-blue-600 to-blue-800 transition-all duration-500 group-hover:w-full mt-1 mx-auto"></div>
            </div>
          </div>
          
          <!-- Desktop Menu - Más espacio entre items -->
          <ul class="hidden md:flex space-x-12 items-center">
            <li 
              v-for="item in [
                { id: 'inicio', name: 'Inicio' },
                { id: 'servicios', name: 'Servicios' },
                { id: 'proceso', name: 'Proceso' },
                { id: 'testimonios', name: 'Testimonios' }
              ]" 
              :key="item.id"
              @click="scrollToSection(item.id)"
              class="cursor-pointer transition-all duration-500 relative group"
              :class="activeSection === item.id ? 'text-blue-600 scale-110' : 'text-gray-600 hover:text-blue-500'"
            >
              <a class="font-semibold text-lg relative z-10 px-2 py-1">{{ item.name }}</a>
              <div 
                class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 h-1 bg-gradient-to-r from-blue-600 to-blue-800 rounded-full transition-all duration-500 origin-center"
                :class="activeSection === item.id ? 'w-full' : 'w-0 group-hover:w-full'"
              ></div>
              <div class="absolute inset-0 bg-blue-600/10 rounded-lg scale-0 group-hover:scale-100 transition-transform duration-500"></div>
            </li>
            <li 
              @click="scrollToSection('contacto')" 
              class="cursor-pointer bg-gradient-to-r from-blue-600 to-blue-800 text-white hover:from-blue-700 hover:to-blue-900 px-10 py-3 rounded-xl transition-all duration-500 transform hover:scale-105 font-semibold shadow-lg hover:shadow-xl relative overflow-hidden group ml-4"
            >
              <span class="relative z-10">Contacto</span>
              <div class="absolute inset-0 bg-white/10 transform scale-x-0 group-hover:scale-x-100 transition-transform duration-500 origin-left"></div>
            </li>
          </ul>

          <!-- Mobile Menu Button -->
          <button 
            @click="toggleMenu" 
            class="md:hidden flex flex-col justify-center items-center w-10 h-10 cursor-pointer relative z-60 bg-gradient-to-br from-blue-600 to-blue-800 rounded-lg shadow-lg"
            aria-label="Menú"
          >
            <span class="w-6 h-0.5 bg-white mb-1 rounded transition-all duration-500" 
                  :class="{ 'rotate-45 translate-y-1.5': isMenuOpen }"></span>
            <span class="w-6 h-0.5 bg-white mb-1 rounded transition-all duration-500" 
                  :class="{ 'opacity-0': isMenuOpen }"></span>
            <span class="w-6 h-0.5 bg-white rounded transition-all duration-500" 
                  :class="{ '-rotate-45 -translate-y-1.5': isMenuOpen }"></span>
          </button>
        </div>

        <!-- Mobile Menu -->
        <div 
          v-if="isMobile && isMenuOpen" 
          class="md:hidden bg-white/95 backdrop-blur-xl border-t border-blue-200/50 py-8 animate-slide-in-down rounded-b-2xl shadow-2xl mt-2 text-center"
        >
          <ul class="space-y-6">
            <li 
              v-for="item in [
                { id: 'inicio', name: 'Inicio' },
                { id: 'servicios', name: 'Servicios' },
                { id: 'proceso', name: 'Proceso' },
                { id: 'testimonios', name: 'Testimonios' }
              ]" 
              :key="item.id"
              @click="scrollToSection(item.id)"
              class="cursor-pointer transition-all duration-500 py-4 px-6 rounded-lg mx-4"
              :class="activeSection === item.id ? 'bg-blue-600/10 text-blue-600 scale-105' : 'text-gray-600 hover:bg-blue-50'"
            >
              <a class="font-semibold text-lg flex items-center justify-center">
                <div class="w-2 h-2 bg-gradient-to-r from-blue-600 to-blue-800 rounded-full mr-4 transition-all duration-500" 
                     :class="activeSection === item.id ? 'scale-100' : 'scale-0'"></div>
                {{ item.name }}
              </a>
            </li>
            <li 
              @click="scrollToSection('contacto')" 
              class="cursor-pointer bg-gradient-to-r from-blue-600 to-blue-800 text-white hover:from-blue-700 hover:to-blue-900 px-8 py-4 rounded-lg transition-all duration-500 transform hover:scale-105 font-semibold shadow-lg mt-6 mx-4 text-center"
            >
              <a>Contacto</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="pt-16 w-full flex flex-col items-center">
      <HeaderInicio />
      <NuestrosServicios />
      <PorqueElegirnos />
      <ProcesoDesarrollo />
      <TestimoniosClientes />
      <Contacto />
    </main>

    <!-- Floating Action Buttons -->
    <div class="fixed bottom-8 right-8 z-40 space-y-4">
      <!-- WhatsApp Button -->
      <button 
        class="w-16 h-16 bg-green-500 hover:bg-green-600 text-white rounded-2xl shadow-2xl flex items-center justify-center transition-all duration-500 transform hover:scale-110 hover:rotate-12 group animate-bounce-slow"
        aria-label="WhatsApp"
      >
        <span class="text-2xl">💬</span>
        <div class="absolute inset-0 bg-white/20 rounded-2xl scale-0 group-hover:scale-100 transition-transform duration-500"></div>
      </button>
      
      <!-- Scroll to Top -->
      <button 
        @click="scrollToSection('inicio')"
        class="w-16 h-16 bg-gradient-to-br from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 text-white rounded-2xl shadow-2xl flex items-center justify-center transition-all duration-500 transform hover:scale-110 hover:-translate-y-1 group"
        aria-label="Volver arriba"
      >
        <span class="text-2xl transform transition-transform duration-500 group-hover:-translate-y-1">↑</span>
        <div class="absolute inset-0 bg-white/10 rounded-2xl scale-0 group-hover:scale-100 transition-transform duration-500"></div>
      </button>
    </div>

    <!-- Footer -->
    <footer class="bg-gradient-to-br from-gray-900 via-blue-900 to-gray-900 text-white py-16 w-full flex justify-center relative overflow-hidden">
      <!-- Background Elements -->
      <div class="absolute inset-0 overflow-hidden">
        <div class="absolute -top-20 -right-20 w-40 h-40 bg-blue-600/10 rounded-full animate-pulse-slow"></div>
        <div class="absolute -bottom-20 -left-20 w-40 h-40 bg-blue-500/10 rounded-full animate-pulse-slower"></div>
        <div class="absolute top-1/2 left-1/4 w-8 h-8 bg-blue-400/20 rounded-full animate-float"></div>
        <div class="absolute bottom-1/3 right-1/4 w-6 h-6 bg-blue-300/20 rounded-full animate-float-delayed"></div>
      </div>
      
      <div class="w-full max-w-7xl mx-auto px-4 relative z-10">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8 text-center md:text-left">
          <!-- Logo y Descripción -->
          <div class="flex flex-col items-center md:items-start">
            <div class="flex items-center space-x-6 justify-center md:justify-start mb-6 group cursor-pointer" @click="scrollToSection('inicio')">
              <div class="w-14 h-14 bg-gradient-to-br from-blue-600 to-blue-800 rounded-xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
                <span class="text-white font-bold text-xl">JMG</span>
              </div>
              <span class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-blue-300 bg-clip-text text-transparent">JMG Desarrollos</span>
            </div>
            <p class="text-gray-400 mb-6 max-w-xs text-center md:text-left leading-relaxed">
              Creamos soluciones web innovadoras que impulsan el crecimiento de tu negocio con tecnología de vanguardia.
            </p>
            <p class="text-gray-500 text-sm text-center md:text-left">&copy; 2024 JMG Desarrollos. Todos los derechos reservados.</p>
          </div>
          
          <!-- Enlaces rápidos -->
          <div class="flex flex-col items-center md:items-start">
            <h3 class="text-lg font-bold mb-6 text-transparent bg-gradient-to-r from-blue-400 to-blue-300 bg-clip-text">Enlaces Rápidos</h3>
            <ul class="space-y-3">
              <li v-for="link in ['inicio', 'servicios', 'proceso', 'testimonios']" :key="link">
                <a 
                  @click="scrollToSection(link)" 
                  class="text-gray-400 hover:text-white transition-all duration-500 cursor-pointer transform hover:translate-x-2 inline-block group"
                >
                  <span class="flex items-center justify-center md:justify-start">
                    <div class="w-1 h-1 bg-gradient-to-r from-blue-400 to-blue-300 rounded-full mr-2 opacity-0 group-hover:opacity-100 transition-all duration-500"></div>
                    {{ link.charAt(0).toUpperCase() + link.slice(1) }}
                  </span>
                </a>
              </li>
            </ul>
          </div>
          
          <!-- Contacto -->
          <div class="flex flex-col items-center md:items-start">
            <h3 class="text-lg font-bold mb-6 text-transparent bg-gradient-to-r from-blue-400 to-blue-300 bg-clip-text">Contacto</h3>
            <div class="space-y-4 text-gray-400 flex flex-col items-center md:items-start">
              <p class="flex items-center transition-all duration-500 hover:text-white transform hover:translate-x-2 group justify-center md:justify-start">
                <span class="w-8 h-8 bg-gradient-to-br from-blue-600 to-blue-800 rounded-full flex items-center justify-center mr-3 group-hover:scale-110 transition-transform duration-500">📞</span>
                +54 9 11 5527-1430
              </p>
              <p class="flex items-center transition-all duration-500 hover:text-white transform hover:translate-x-2 group justify-center md:justify-start">
                <span class="w-8 h-8 bg-gradient-to-br from-blue-600 to-blue-800 rounded-full flex items-center justify-center mr-3 group-hover:scale-110 transition-transform duration-500">✉️</span>
                contacto@jmgdesarrollos.com
              </p>
              <p class="flex items-center transition-all duration-500 hover:text-white transform hover:translate-x-2 group justify-center md:justify-start">
                <span class="w-8 h-8 bg-gradient-to-br from-blue-600 to-blue-800 rounded-full flex items-center justify-center mr-3 group-hover:scale-110 transition-transform duration-500">📍</span>
                Buenos Aires, Argentina
              </p>
            </div>
          </div>
          
          <!-- Redes sociales -->
          <div class="flex flex-col items-center md:items-start">
            <h3 class="text-lg font-bold mb-6 text-transparent bg-gradient-to-r from-blue-400 to-blue-300 bg-clip-text">Síguenos</h3>
            <div class="flex justify-center md:justify-start space-x-3">
              <a 
                v-for="(social, index) in [
                  { name: 'FB', icon: '📘', color: 'from-blue-600 to-blue-800' },
                  { name: 'IG', icon: '📷', color: 'from-blue-500 to-blue-700' },
                  { name: 'IN', icon: '💼', color: 'from-blue-700 to-blue-900' },
                  { name: 'WA', icon: '💚', color: 'from-blue-600 to-blue-800' }
                ]" 
                :key="social.name" 
                href="#" 
                class="w-12 h-12 bg-gradient-to-br rounded-xl flex items-center justify-center transition-all duration-500 transform hover:scale-110 hover:-translate-y-1 shadow-lg"
                :class="social.color"
              >
                <span class="text-white font-bold text-lg">{{ social.icon }}</span>
              </a>
            </div>
          </div>
        </div>
        
        <!-- Divider -->
        <div class="border-t border-blue-700/50 mt-12 pt-8 text-center">
          <p class="text-gray-500 text-sm">
            Hecho con ❤️ por JMG Desarrollos - Transformando ideas en realidad digital
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>