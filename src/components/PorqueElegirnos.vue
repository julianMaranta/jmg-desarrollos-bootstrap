<template>
  <section class="py-12 bg-gradient-to-br from-white via-blue-50 to-blue-100 relative overflow-hidden w-full flex justify-center">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-0 right-0 w-96 h-96 bg-blue-500/5 rounded-full animate-float-delayed blur-3xl"></div>
      <div class="absolute bottom-0 left-0 w-96 h-96 bg-blue-400/5 rounded-full animate-float blur-3xl"></div>
    </div>

    <div class="w-full max-w-7xl mx-auto px-4 relative z-10 flex flex-col items-center">
      <!-- Section Header -->
      <div class="text-center mb-16 w-full flex flex-col items-center">
        <!-- MÁS ESPACIO DEBAJO DE "🎯 POR QUÉ ELEGIRNOS" -->
        <div class="inline-flex items-center bg-white/80 backdrop-blur-sm rounded-full px-6 py-3 mb-16 border border-blue-200 shadow-lg">
          <div class="w-2 h-2 bg-gradient-to-r from-blue-600 to-blue-800 rounded-full mr-3 animate-pulse"></div>
          <span class="text-sm font-semibold text-gray-600">🎯 POR QUÉ ELEGIRNOS</span>
        </div>

        <!-- ESPACIO EXTRA ANTES DE TECHNOLOGY & PROMISE -->
      <div class="h-5 w-full"></div>
        
        <h2 class="text-5xl md:text-6xl font-black mb-8 bg-gradient-to-r from-gray-800 via-blue-800 to-blue-900 bg-clip-text text-transparent text-center w-full h-full">
          Ventajas Exclusivas
        </h2>
        <!-- ESPACIO AUMENTADO DEBAJO DE ESTE TÍTULO - mb-20 cambiado a mb-24 -->
        <p class="text-xl text-gray-600 max-w-3xl leading-relaxed text-center mx-auto mb-24">
          No solo desarrollamos sitios web, creamos <span class="font-semibold text-blue-600">experiencias digitales</span> que impulsan tu negocio
        </p>
      </div>

      <!-- ESPACIO EXTRA ANTES DE TECHNOLOGY & PROMISE -->
      <div class="h-10 w-full"></div>

      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16 w-full justify-items-center">
        <div v-for="(feature, index) in features" :key="index" 
             class="group text-center p-8 bg-white/80 backdrop-blur-sm rounded-3xl shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-4 border border-blue-200/50 w-full max-w-xs flex flex-col items-center">
          <!-- Icon Container -->
          <div class="relative mb-6 flex justify-center">
            <div class="w-20 h-20 bg-gradient-to-br from-blue-600 to-blue-800 rounded-2xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
              <span class="text-2xl text-white flex items-center justify-center w-full h-full">{{ feature.icon }}</span>
            </div>
            <div class="absolute -inset-4 bg-gradient-to-br from-blue-600/20 to-blue-800/20 rounded-2xl blur-xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          </div>
          
          <!-- Content -->
          <h3 class="text-xl font-black text-gray-800 mb-4 text-center">{{ feature.title }}</h3>
          <p class="text-gray-600 leading-relaxed text-center">
            {{ feature.description }}
          </p>
          
          <!-- Hover Effect Line -->
          <div class="w-0 h-1 bg-gradient-to-r from-blue-600 to-blue-800 rounded-full mt-6 transition-all duration-500 group-hover:w-16"></div>
        </div>
      </div>

      <!-- ESPACIO EXTRA ANTES DE TECHNOLOGY & PROMISE -->
      <div class="h-16 w-full"></div>

      <!-- Technology & Promise Section -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center w-full max-w-6xl">
        <!-- Technology Stack -->
        <div class="text-center lg:text-left flex flex-col items-center lg:items-start">
          <h3 class="text-4xl font-black text-gray-800 mb-8 bg-gradient-to-r from-gray-800 to-blue-800 bg-clip-text text-transparent text-center w-full">
            Tecnología de Vanguardia
          </h3>
          <p class="text-lg text-gray-600 mb-8 leading-relaxed text-center lg:text-left w-full">
            Utilizamos el stack tecnológico más moderno para garantizar que tu sitio web sea 
            <span class="font-semibold text-blue-600">rápido, seguro y escalable</span>.
          </p>
          
          <div class="grid grid-cols-2 gap-6 w-full">
            <div v-for="(tech, index) in technologies" :key="index" 
                 class="flex items-center space-x-4 p-4 bg-white/50 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105 group justify-center lg:justify-start">
              <div class="w-12 h-12 bg-gradient-to-br from-blue-600 to-blue-800 rounded-xl flex items-center justify-center transform transition-all duration-300 group-hover:rotate-12">
                <span class="text-white font-bold text-sm flex items-center justify-center w-full h-full">{{ tech.icon }}</span>
              </div>
              <div class="text-center lg:text-left">
                <div class="font-black text-gray-800">{{ tech.name }}</div>
                <div class="text-sm text-gray-500">{{ tech.description }}</div>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Our Promise - UBICADA MÁS ABAJO Y CON MÁS SEPARACIÓN -->
        <div class="relative flex justify-center mt-8">
          <div class="bg-gradient-to-br from-blue-600 via-blue-700 to-blue-800 rounded-3xl p-8 text-white shadow-2xl relative overflow-hidden w-full max-w-md">
            <!-- Background Pattern -->
            <div class="absolute inset-0 opacity-10">
              <div class="absolute inset-0" style="background-image: radial-gradient(circle, white 1px, transparent 1px); background-size: 20px 20px;"></div>
            </div>
            
            <div class="relative z-10">
              <h4 class="text-3xl font-black mb-8 text-center w-full">Nuestra Promesa</h4>
              <div class="h-5 w-full"></div>
              <div class="space-y-8">
                
                <div v-for="(promise, index) in promises" :key="index" 
                     class="flex items-center p-4 bg-white/10 rounded-2xl backdrop-blur-sm transform transition-all duration-300 hover:scale-105 group justify-center lg:justify-start">
                     
                  <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center mr-4 transform transition-all duration-300 group-hover:rotate-12">
                    <span class="text-white text-xl flex items-center justify-center w-full h-full">✓</span>
                  </div>
                  
                  <div class="text-center lg:text-left">
                    <div class="font-bold text-lg">{{ promise.title }}</div>
                    <div class="text-white/80 text-sm">{{ promise.description }}</div>
                  </div>
                  
                </div>
                
              </div>
            </div>
          </div>
        </div>
      </div>

      
      <div class="h-10 w-full"></div>

      <!-- CTA Section - MODIFICADA PARA CENTRAR VERTICALMENTE LOS TEXTOS -->
      <div class="text-center w-full flex flex-col items-center justify-center">
        <div class="bg-gradient-to-r from-blue-500/10 to-blue-600/10 rounded-3xl p-12 border border-blue-500/20 w-full max-w-4xl">
          <div class="flex flex-col items-center justify-center space-y-8">
            <h3 class="text-3xl md:text-4xl font-black text-gray-800 text-center w-full">
              ¿Listo para Transformar tu Presencia Digital?
            </h3>
            <p class="text-xl text-gray-600 max-w-2xl mx-auto text-center">
              Únete a más de 200 empresas que ya confían en nosotros para llevar su negocio al siguiente nivel.
            </p>
            <div class="h-5 w-full"></div>
            <button 
              @click="scrollToSection('contacto')"
              class="bg-gradient-to-r from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 text-white font-black py-4 px-12 rounded-2xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 shadow-2xl hover:shadow-3xl text-lg relative overflow-hidden group"
            >
              <span class="relative z-10 flex items-center justify-center">
                Comenzar Proyecto
                <span class="ml-3 transform transition-transform duration-500 group-hover:translate-x-2">🚀</span>
              </span>
              <div class="absolute inset-0 bg-white/20 transform -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    icon: '⚡',
    title: 'Desarrollo Express',
    description: 'Entregamos proyectos en tiempo récord sin comprometer la calidad y atención al detalle.'
  },
  {
    icon: '💎',
    title: 'Calidad Premium',
    description: 'Código limpio, arquitectura escalable y mejores prácticas de desarrollo web moderno.'
  },
  {
    icon: '🛡️',
    title: 'Soporte Continuo',
    description: 'No te dejamos solo. Soporte técnico post-entrega y actualizaciones regulares.'
  },
  {
    icon: '🎯',
    title: 'Enfoque en ROI',
    description: 'Desarrollamos pensando en tus objetivos de negocio y maximización de conversiones.'
  }
];

const technologies = [
  {
    icon: '⚛️',
    name: 'React & Vue.js',
    description: 'Frameworks modernos'
  },
  {
    icon: '🚀',
    name: 'Node.js',
    description: 'Backend escalable'
  },
  {
    icon: '🗄️',
    name: 'MongoDB',
    description: 'Base de datos NoSQL'
  },
  {
    icon: '☁️',
    name: 'AWS & Vercel',
    description: 'Cloud hosting'
  }
];

const promises = [
  {
    title: 'Entrega Puntual',
    description: 'Cumplimos con los plazos establecidos sin excusas'
  },
  {
    title: 'Comunicación Transparente',
    description: 'Mantenemos un canal abierto durante todo el proyecto'
  },
  {
    title: 'Satisfacción Garantizada',
    description: 'Trabajamos hasta que estés 100% satisfecho'
  },
  {
    title: 'Soporte Post-Entrega',
    description: 'No te abandonamos después del lanzamiento'
  }
];

const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>