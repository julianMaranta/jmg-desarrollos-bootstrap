<template>
  <section id="testimonios" class="py-20 bg-gradient-to-br from-white via-blue-50 to-blue-100 relative overflow-hidden w-full flex justify-center items-center">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-0 right-0 w-96 h-96 bg-blue-500/5 rounded-full animate-float-delayed blur-3xl"></div>
      <div class="absolute bottom-0 left-0 w-96 h-96 bg-blue-400/5 rounded-full animate-float blur-3xl"></div>
    </div>

    <div class="w-full max-w-7xl mx-auto px-4 relative z-10 flex flex-col items-center justify-center">
      <!-- Section Header -->
      <div class="text-center mb-20 w-full flex flex-col items-center">
        <div class="inline-flex items-center bg-white/80 backdrop-blur-sm rounded-full px-6 py-3 mb-6 border border-blue-200 shadow-lg justify-center">
          <div class="w-2 h-2 bg-gradient-to-r from-blue-600 to-blue-800 rounded-full mr-3 animate-pulse"></div>
          <span class="text-sm font-semibold text-gray-600">💬 LO QUE DICEN NUESTROS CLIENTES</span>
        </div>

        <div class="h-5 w-full"></div>
        
        <h2 class="text-5xl md:text-6xl font-black mb-6 bg-gradient-to-r from-gray-800 via-blue-800 to-blue-900 bg-clip-text text-transparent text-center w-full">
          Historias de Éxito
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto leading-relaxed text-center">
          Más de 200 empresas confían en nosotros para transformar su presencia digital y alcanzar nuevos niveles de crecimiento
        </p>
      </div>

      <div class="h-10 w-full"></div>

      <!-- Testimonials Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16 w-full justify-items-center">
        <!-- Testimonio 1 -->
        <div class="group bg-white/80 backdrop-blur-sm rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-4 border border-blue-200/50 w-full max-w-sm flex flex-col items-center text-center">
          <!-- Header -->
          <div class="flex flex-col items-center mb-6 w-full">
            <div class="w-16 h-16 bg-gradient-to-br from-blue-600 to-blue-800 rounded-2xl flex items-center justify-center mb-4 transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
              <span class="text-white font-bold text-xl">MR</span>
            </div>
            <div class="text-center w-full">
              <h4 class="font-black text-gray-800 text-lg">María Rodríguez</h4>
              <p class="text-gray-500 text-sm">Dueña de Boutique Elegante</p>
            </div>
          </div>
          
          <!-- Rating -->
          <div class="flex mb-4 justify-center w-full">
            <span v-for="star in 5" :key="star" class="text-yellow-400 text-lg">⭐</span>
          </div>
          
          <!-- Testimonial Text -->
          <p class="text-gray-600 leading-relaxed italic mb-6 w-full text-center">
            "JMG Desarrollos transformó completamente mi negocio. Mi sitio web no solo es hermoso, sino que ha aumentado mis ventas online en un 300%. El equipo es profesional y muy comprometido con el éxito del proyecto."
          </p>
          
          <!-- Results -->
          <div class="bg-gradient-to-r from-blue-50 to-blue-100 rounded-2xl p-4 border border-blue-200 w-full">
            <div class="flex justify-between items-center text-sm">
              <span class="text-blue-600 font-semibold">Resultados:</span>
              <span class="text-green-600 font-black">+300% Ventas</span>
            </div>
          </div>
        </div>

        <!-- Testimonio 2 -->
        <div class="group bg-white/80 backdrop-blur-sm rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-4 border border-blue-200/50 w-full max-w-sm flex flex-col items-center text-center">
          <!-- Header -->
          <div class="flex flex-col items-center mb-6 w-full">
            <div class="w-16 h-16 bg-gradient-to-br from-blue-700 to-blue-900 rounded-2xl flex items-center justify-center mb-4 transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
              <span class="text-white font-bold text-xl">CP</span>
            </div>
            <div class="text-center w-full">
              <h4 class="font-black text-gray-800 text-lg">Carlos Pérez</h4>
              <p class="text-gray-500 text-sm">Director de TechSolutions</p>
            </div>
          </div>
          
          <!-- Rating -->
          <div class="flex mb-4 justify-center w-full">
            <span v-for="star in 5" :key="star" class="text-yellow-400 text-lg">⭐</span>
          </div>
          
          <!-- Testimonial Text -->
          <p class="text-gray-600 leading-relaxed italic mb-6 w-full text-center">
            "Trabajamos con JMG para nuestro sitio corporativo y los resultados superaron expectativas. El proceso fue transparente, la comunicación excelente y la entrega fue puntual. Definitivamente los recomiendo."
          </p>
          
          <!-- Results -->
          <div class="bg-gradient-to-r from-blue-100 to-blue-200 rounded-2xl p-4 border border-blue-300 w-full">
            <div class="flex justify-between items-center text-sm">
              <span class="text-blue-600 font-semibold">Resultados:</span>
              <span class="text-green-600 font-black">+150% Leads</span>
            </div>
          </div>
        </div>

        <!-- Testimonio 3 -->
        <div class="group bg-white/80 backdrop-blur-sm rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 transform hover:-translate-y-4 border border-blue-200/50 w-full max-w-sm flex flex-col items-center text-center">
          <!-- Header -->
          <div class="flex flex-col items-center mb-6 w-full">
            <div class="w-16 h-16 bg-gradient-to-br from-blue-800 to-blue-950 rounded-2xl flex items-center justify-center mb-4 transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
              <span class="text-white font-bold text-xl">AG</span>
            </div>
            <div class="text-center w-full">
              <h4 class="font-black text-gray-800 text-lg">Ana García</h4>
              <p class="text-gray-500 text-sm">Fundadora de Wellness Center</p>
            </div>
          </div>
          
          <!-- Rating -->
          <div class="flex mb-4 justify-center w-full">
            <span v-for="star in 5" :key="star" class="text-yellow-400 text-lg">⭐</span>
          </div>
          
          <!-- Testimonial Text -->
          <p class="text-gray-600 leading-relaxed italic mb-6 w-full text-center">
            "Increíble experiencia de principio a fin. Mi sitio web captura perfectamente la esencia de mi marca y ha sido clave para atraer nuevos clientes. El soporte post-venta es excepcional y siempre están disponibles."
          </p>
          
          <!-- Results -->
          <div class="bg-gradient-to-r from-blue-200 to-blue-300 rounded-2xl p-4 border border-blue-400 w-full">
            <div class="flex justify-between items-center text-sm">
              <span class="text-blue-600 font-semibold">Resultados:</span>
              <span class="text-green-600 font-black">+200% Clientes</span>
            </div>
          </div>
        </div>
      </div>

      <div class="h-10 w-full"></div>

     <!-- Client Logos -->
<div class="text-center w-full flex flex-col items-center">
  <h3 class="text-2xl font-black text-gray-800 mb-12 bg-gradient-to-r from-gray-800 to-blue-800 bg-clip-text text-transparent text-center w-full">
    Empresas que Confían en Nosotros
  </h3>
  <div class="h-5 w-full"></div>
  <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-8 items-center opacity-60 justify-items-center w-full">
    <div v-for="i in 6" :key="i" 
         class="bg-white/80 backdrop-blur-sm rounded-2xl h-24 flex flex-col items-center justify-center shadow-lg hover:shadow-xl transition-all duration-500 transform hover:scale-110 group border border-blue-200/50 w-full max-w-40">
      <div class="text-center w-full flex flex-col items-center justify-center">
        <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-800 rounded-xl flex items-center justify-center mb-2 transform transition-all duration-500 group-hover:rotate-12">
          <span class="text-white font-bold text-sm flex items-center justify-center w-full">C{{ i }}</span>
        </div>
        <span class="text-gray-600 font-semibold text-sm text-center w-full">Cliente {{ i }}</span>
      </div>
    </div>
  </div>
</div>

      <div class="h-10 w-full"></div>

     <!-- CTA Section -->
<div class="text-center mt-20 w-full">
  <div class="bg-gradient-to-r from-blue-500/10 to-blue-600/10 rounded-3xl p-12 border border-blue-500/20 w-full flex flex-col items-center justify-center">
    <h3 class="text-3xl md:text-4xl font-black text-gray-800 mb-6 text-center w-full">
      ¿Listo para ser Nuestro Próximo Caso de Éxito?
    </h3>
    
    <div class="flex items-center justify-center w-full mb-8">
      <p class="text-xl text-gray-600 max-w-2xl text-center leading-relaxed">
        Únete a las empresas que ya experimentaron la transformación digital con JMG Desarrollos.
      </p>
    </div>

    <div class="h-5 w-full"></div>

    <div class="flex justify-center w-full">
      <button 
        @click="scrollToSection('contacto')"
        class="bg-gradient-to-r from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 text-white font-black py-4 px-12 rounded-2xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 shadow-2xl hover:shadow-3xl text-lg relative overflow-hidden group"
      >
        <span class="relative z-10 flex items-center justify-center">
          Unirme al Éxito
          <span class="ml-3 transform transition-transform duration-500 group-hover:translate-x-2">🎉</span>
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