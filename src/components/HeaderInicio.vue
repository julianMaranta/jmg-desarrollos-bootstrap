<template>
  <header id="inicio" class="min-h-[80vh] w-full bg-gradient-to-br from-blue-900 via-blue-800 to-blue-900 text-white relative overflow-hidden flex items-center justify-center">
    <!-- Animated Background -->
    <div class="absolute inset-0 overflow-hidden w-full">
      <!-- Floating Particles -->
      <div v-for="i in 20" :key="i" 
           class="absolute w-2 h-2 bg-white/10 rounded-full animate-float"
           :style="{
             left: Math.random() * 100 + '%',
             top: Math.random() * 100 + '%',
             animationDelay: Math.random() * 5 + 's',
             animationDuration: 3 + Math.random() * 2 + 's'
           }">
      </div>
      
      <!-- Gradient Orbs -->
      <div class="absolute -top-40 -right-40 w-96 h-96 bg-blue-600/20 rounded-full animate-pulse-slow blur-3xl"></div>
      <div class="absolute -bottom-40 -left-40 w-96 h-96 bg-blue-500/20 rounded-full animate-pulse-slower blur-3xl"></div>
      <div class="absolute top-1/3 left-1/4 w-32 h-32 bg-blue-400/10 rounded-full animate-float-delayed blur-2xl"></div>
      <div class="absolute bottom-1/4 right-1/3 w-24 h-24 bg-blue-300/10 rounded-full animate-float blur-2xl"></div>
      
      <!-- Grid Pattern -->
      <div class="absolute inset-0 opacity-10 w-full">
        <div class="absolute inset-0 w-full" style="background-image: linear-gradient(rgba(255,255,255,0.1) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.1) 1px, transparent 1px); background-size: 50px 50px;"></div>
      </div>
    </div>
    
    <div class="w-full px-4 text-center relative z-10 py-16 flex flex-col items-center">
      <!-- Main Content -->
      <div class="animate-fade-in-up w-full flex flex-col items-center">
        <!-- Badge -->
        <div class="inline-flex items-center bg-white/10 backdrop-blur-sm rounded-full px-6 py-3 mb-12 border border-white/20 animate-pulse">
          <div class="w-2 h-2 bg-blue-400 rounded-full mr-3 animate-ping"></div>
          <span class="text-sm font-semibold text-white/80">🚀 Listos para impulsar tu negocio</span>
        </div>

        <!-- Main Heading -->
        <h1 class="text-5xl md:text-7xl lg:text-8xl font-black mb-12 leading-tight text-center w-full">
          <span class="block animate-slide-in-left bg-gradient-to-r from-white via-blue-200 to-blue-100 bg-clip-text text-transparent mb-4">
            Impulsa Tu
          </span>
          <span class="block animate-slide-in-right delay-300 bg-gradient-to-r from-blue-200 via-blue-100 to-white bg-clip-text text-transparent">
            Negocio Digital
          </span>
        </h1>

        <!-- Subheading -->
        <p class="text-xl md:text-2xl lg:text-3xl mb-20 text-white/80 max-w-6xl mx-auto leading-relaxed animate-fade-in-up delay-500 text-center w-full px-4">
          Creamos <span class="text-blue-300 font-semibold">experiencias web extraordinarias</span> que convierten visitantes en clientes leales
        </p>

        <!-- CTA Buttons - CON MÁS ESPACIO ARRIBA Y ABAJO -->
        <div class="flex flex-col sm:flex-row gap-8 justify-center items-center py-10 my-8 animate-fade-in-up delay-700 w-full">
          <button 
            @click="scrollToSection('servicios')"
            class="group relative bg-gradient-to-r from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 text-white font-bold py-6 px-14 rounded-2xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 shadow-2xl hover:shadow-3xl text-lg overflow-hidden"
          >
            <span class="relative z-10 flex items-center">
              Explorar Servicios
              <span class="ml-3 transform transition-transform duration-500 group-hover:translate-x-1">→</span>
            </span>
            <div class="absolute inset-0 bg-white/20 transform -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
          </button>
          
          <button 
            @click="scrollToSection('contacto')"
            class="group relative bg-transparent border-2 border-white/30 hover:border-white text-white hover:bg-white/10 font-bold py-6 px-14 rounded-2xl transition-all duration-500 transform hover:scale-105 text-lg backdrop-blur-sm overflow-hidden"
          >
            <span class="relative z-10 flex items-center">
              <span class="mr-3">💬</span>
              Contactar Ahora
            </span>
            <div class="absolute inset-0 bg-white/5 transform scale-0 group-hover:scale-100 transition-transform duration-500 rounded-2xl"></div>
          </button>
        </div>

        <!-- Stats -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-12 max-w-6xl mx-auto animate-fade-in-up delay-1000 w-full px-4 mt-20">
          <div v-for="(stat, index) in stats" :key="index" 
               class="text-center transform transition-all duration-500 hover:scale-110 group">
            <div class="relative">
              <div class="text-3xl md:text-5xl font-black text-white mb-4 animate-count-up" 
                   :data-target="stat.value"
                   :class="stat.gradient">
                {{ stat.value }}
              </div>
              <div class="absolute inset-0 text-3xl md:text-5xl font-black opacity-20 blur-sm group-hover:opacity-30 transition-opacity duration-500"
                   :class="stat.gradient">
                {{ stat.value }}
              </div>
            </div>
            <div class="text-white/60 text-sm font-semibold uppercase tracking-wider">{{ stat.label }}</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Floating Elements -->
    <div class="absolute top-20 left-10 w-6 h-6 bg-blue-400/20 rounded-full animate-float-delayed"></div>
    <div class="absolute top-40 right-20 w-4 h-4 bg-blue-300/20 rounded-full animate-float"></div>
    <div class="absolute bottom-40 left-20 w-5 h-5 bg-blue-200/20 rounded-full animate-float-delayed"></div>
  </header>
</template>

<script setup>
const stats = [
  { 
    value: 200, 
    label: 'Proyectos Entregados',
    gradient: 'bg-gradient-to-r from-blue-400 to-blue-300 bg-clip-text text-transparent'
  },
  { 
    value: 98, 
    label: 'Clientes Satisfechos',
    gradient: 'bg-gradient-to-r from-blue-300 to-blue-200 bg-clip-text text-transparent'
  },
  { 
    value: 24, 
    label: 'Soporte Técnico',
    gradient: 'bg-gradient-to-r from-blue-200 to-blue-100 bg-clip-text text-transparent'
  },
  { 
    value: 5, 
    label: 'Años de Experiencia',
    gradient: 'bg-gradient-to-r from-blue-100 to-white bg-clip-text text-transparent'
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
            counter.textContent = target + (counter.textContent.includes('%') ? '%' : '+');
            clearInterval(timer);
          } else {
            counter.textContent = Math.floor(current) + (counter.textContent.includes('%') ? '%' : '+');
          }
        }, 16);
        
        observer.unobserve(counter);
      }
    });
  }, { threshold: 0.5 });
  
  counters.forEach(counter => observer.observe(counter));
});
</script>