<template>
  <section id="proceso" class="py-20 bg-gradient-to-br from-blue-900 via-blue-800 to-blue-900 text-white relative overflow-hidden w-full flex justify-center">
    <!-- Animated Background -->
    <div class="absolute inset-0 overflow-hidden">
      <!-- Floating Particles -->
      <div v-for="i in 15" :key="i" 
           class="absolute w-1 h-1 bg-white/20 rounded-full animate-float"
           :style="{
             left: Math.random() * 100 + '%',
             top: Math.random() * 100 + '%',
             animationDelay: Math.random() * 3 + 's',
             animationDuration: 2 + Math.random() * 2 + 's'
           }">
      </div>
      
      <!-- Gradient Orbs -->
      <div class="absolute -top-40 -left-40 w-80 h-80 bg-blue-600/10 rounded-full animate-pulse-slow blur-3xl"></div>
      <div class="absolute -bottom-40 -right-40 w-80 h-80 bg-blue-500/10 rounded-full animate-pulse-slower blur-3xl"></div>
    </div>

    <div class="w-full max-w-7xl mx-auto px-4 relative z-10 flex flex-col items-center">
      <!-- Section Header -->
      <div class="text-center mb-20 w-full flex flex-col items-center">
        <div class="inline-flex items-center bg-white/10 backdrop-blur-sm rounded-full px-6 py-3 mb-6 border border-white/20">
          <div class="w-2 h-2 bg-blue-400 rounded-full mr-3 animate-pulse"></div>
          <span class="text-sm font-semibold text-white/80">🔄 NUESTRO PROCESO</span>
        </div>
        
<div class="h-5 w-full"></div>

        <h2 class="text-5xl md:text-6xl font-black mb-6 bg-gradient-to-r from-white via-blue-200 to-blue-100 bg-clip-text text-transparent text-center w-full h-full">
          Metodología Probada
        </h2>
        
        <p class="text-xl text-white/80 max-w-3xl leading-relaxed text-center mx-auto">
          Un proceso estructurado que garantiza el éxito de tu proyecto desde el primer día hasta el lanzamiento
        </p>
      </div>

      <div class="h-10 w-full"></div>

      <!-- Process Timeline -->
      <div class="relative w-full">
        <!-- Timeline Line -->
        <div class="hidden lg:block absolute left-1/2 top-0 bottom-0 w-1 bg-gradient-to-b from-blue-500/50 to-blue-400/50 transform -translate-x-1/2"></div>
        
        <!-- Process Steps -->
        <div class="w-full">
          <!-- Step 1 -->
          <div class="flex flex-col lg:flex-row items-center lg:items-start gap-8 group w-full mb-32">
            <!-- Content -->
            <div class="lg:w-1/2 lg:pr-12 order-2 lg:order-1 flex justify-center lg:justify-end">
              <div class="bg-white/10 backdrop-blur-sm rounded-3xl p-8 border border-white/20 shadow-2xl transform transition-all duration-500 group-hover:scale-105 w-full max-w-lg">
                <div class="flex items-center justify-center mb-6">
                  <div class="w-16 h-16 bg-gradient-to-br from-blue-500 to-blue-700 rounded-2xl flex items-center justify-center text-white font-black text-2xl shadow-lg transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6">
                    1
                  </div>
                </div>
                <h3 class="text-3xl font-black text-white mb-4 text-center">Descubrimiento & Estrategia</h3>
                <p class="text-white/80 leading-relaxed text-lg text-center">
                  Comprendemos profundamente tu negocio, objetivos y audiencia para crear una estrategia digital personalizada que impulse tus resultados.
                </p>
                <ul class="mt-6 space-y-3 text-white/70">
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Análisis de competencia</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Definición de objetivos</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Planificación estratégica</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <!-- Visual -->
            <div class="lg:w-1/2 lg:pl-12 order-1 lg:order-2 flex justify-center lg:justify-start">
              <div class="w-48 h-48 bg-gradient-to-br from-blue-500/20 to-blue-600/20 rounded-3xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3 shadow-2xl border border-white/10">
                <span class="text-6xl">💡</span>
              </div>
            </div>
          </div>

          <div class="h-10 w-full"></div>

          <!-- Step 2 -->
          <div class="flex flex-col lg:flex-row items-center lg:items-start gap-8 group w-full mb-32">
            <!-- Visual -->
            <div class="lg:w-1/2 lg:pr-12 order-1 flex justify-center lg:justify-end">
              <div class="w-48 h-48 bg-gradient-to-br from-blue-600/20 to-blue-700/20 rounded-3xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3 shadow-2xl border border-white/10">
                <span class="text-6xl">🎨</span>
              </div>
            </div>
            
            <!-- Content -->
            <div class="lg:w-1/2 lg:pl-12 order-2 flex justify-center lg:justify-start">
              <div class="bg-white/10 backdrop-blur-sm rounded-3xl p-8 border border-white/20 shadow-2xl transform transition-all duration-500 group-hover:scale-105 w-full max-w-lg">
                <div class="flex items-center justify-center mb-6">
                  <div class="w-16 h-16 bg-gradient-to-br from-blue-600 to-blue-800 rounded-2xl flex items-center justify-center text-white font-black text-2xl shadow-lg transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6">
                    2
                  </div>
                </div>
                <h3 class="text-3xl font-black text-white mb-4 text-center">Diseño & Experiencia</h3>
                <p class="text-white/80 leading-relaxed text-lg text-center">
                  Creamos diseños visualmente impactantes y experiencias de usuario fluidas que reflejan tu marca y optimizan la conversión.
                </p>
                <ul class="mt-6 space-y-3 text-white/70">
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Wireframes y prototipos</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Diseño UI/UX personalizado</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Pruebas de usabilidad</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <div class="h-10 w-full"></div>

          <!-- Step 3 -->
          <div class="flex flex-col lg:flex-row items-center lg:items-start gap-8 group w-full mb-32">
            <!-- Content -->
            <div class="lg:w-1/2 lg:pr-12 order-2 lg:order-1 flex justify-center lg:justify-end">
              <div class="bg-white/10 backdrop-blur-sm rounded-3xl p-8 border border-white/20 shadow-2xl transform transition-all duration-500 group-hover:scale-105 w-full max-w-lg">
                <div class="flex items-center justify-center mb-6">
                  <div class="w-16 h-16 bg-gradient-to-br from-blue-700 to-blue-900 rounded-2xl flex items-center justify-center text-white font-black text-2xl shadow-lg transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6">
                    3
                  </div>
                </div>
                <h3 class="text-3xl font-black text-white mb-4 text-center">Desarrollo & Implementación</h3>
                <p class="text-white/80 leading-relaxed text-lg text-center">
                  Programamos tu sitio web con las mejores tecnologías, asegurando máximo rendimiento, seguridad y escalabilidad para el futuro.
                </p>
                <ul class="mt-6 space-y-3 text-white/70">
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Desarrollo frontend y backend</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Integración de funcionalidades</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Optimización SEO técnico</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <!-- Visual -->
            <div class="lg:w-1/2 lg:pl-12 order-1 lg:order-2 flex justify-center lg:justify-start">
              <div class="w-48 h-48 bg-gradient-to-br from-blue-700/20 to-blue-800/20 rounded-3xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3 shadow-2xl border border-white/10">
                <span class="text-6xl">⚡</span>
              </div>
            </div>
          </div>

          <div class="h-10 w-full"></div>

          <!-- Step 4 -->
          <div class="flex flex-col lg:flex-row items-center lg:items-start gap-8 group w-full mb-32">
            <!-- Visual -->
            <div class="lg:w-1/2 lg:pr-12 order-1 flex justify-center lg:justify-end">
              <div class="w-48 h-48 bg-gradient-to-br from-blue-800/20 to-blue-900/20 rounded-3xl flex items-center justify-center transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3 shadow-2xl border border-white/10">
                <span class="text-6xl">🚀</span>
              </div>
            </div>
            
            <!-- Content -->
            <div class="lg:w-1/2 lg:pl-12 order-2 flex justify-center lg:justify-start">
              <div class="bg-white/10 backdrop-blur-sm rounded-3xl p-8 border border-white/20 shadow-2xl transform transition-all duration-500 group-hover:scale-105 w-full max-w-lg">
                <div class="flex items-center justify-center mb-6">
                  <div class="w-16 h-16 bg-gradient-to-br from-blue-800 to-blue-950 rounded-2xl flex items-center justify-center text-white font-black text-2xl shadow-lg transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6">
                    4
                  </div>
                </div>
                <h3 class="text-3xl font-black text-white mb-4 text-center">Lanzamiento & Crecimiento</h3>
                <p class="text-white/80 leading-relaxed text-lg text-center">
                  Desplegamos tu sitio web y proporcionamos soporte continuo para garantizar su éxito a largo plazo y crecimiento constante.
                </p>
                <ul class="mt-6 space-y-3 text-white/70">
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Lanzamiento y deployment</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Monitoreo y analytics</span>
                  </li>
                  <li class="flex items-center justify-center">
                    <div class="w-2 h-2 bg-blue-400 rounded-full mr-3"></div>
                    <span>Soporte y mantenimiento</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="h-10 w-full"></div>

      <!-- CTA Section -->
<div class="text-center mt-20 w-full flex flex-col items-center justify-center">
  <div class="bg-gradient-to-r from-blue-500/20 to-blue-600/20 rounded-3xl p-12 border border-blue-500/30 w-full max-w-4xl mx-auto flex flex-col items-center justify-center">
    <h3 class="text-3xl md:text-4xl font-black text-white mb-6 text-center w-full">
      ¿Listo para Iniciar tu Proyecto?
    </h3>
    <p class="text-xl text-white/80 mb-8 max-w-2xl text-center">
      Sigue los pasos de más de 200 empresas exitosas que confiaron en nuestro proceso probado.
    </p>
    <div class="h-5 w-full"></div>
    <div class="flex justify-center w-full">
      <button 
        @click="scrollToSection('contacto')"
        class="bg-gradient-to-r from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 text-white font-black py-4 px-12 rounded-2xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 shadow-2xl hover:shadow-3xl text-lg relative overflow-hidden group"
      >
        <span class="relative z-10 flex items-center justify-center">
          Iniciar Proceso
          <span class="ml-3 transform transition-transform duration-500 group-hover:translate-x-2">🎯</span>
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
const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>