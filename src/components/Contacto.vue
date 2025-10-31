<template>
  <section id="contacto" class="py-20 bg-gradient-to-br from-blue-900 via-blue-800 to-blue-900 text-white relative overflow-hidden w-full flex justify-center items-center">
    <!-- Animated Background -->
    <div class="absolute inset-0 overflow-hidden">
      <!-- Floating Particles -->
      <div v-for="i in 12" :key="i" 
           class="absolute w-1 h-1 bg-white/30 rounded-full animate-float"
           :style="{
             left: Math.random() * 100 + '%',
             top: Math.random() * 100 + '%',
             animationDelay: Math.random() * 4 + 's',
             animationDuration: 3 + Math.random() * 2 + 's'
           }">
      </div>
      
      <!-- Gradient Orbs -->
      <div class="absolute -top-20 -right-20 w-64 h-64 bg-blue-600/10 rounded-full animate-pulse-slow blur-3xl"></div>
      <div class="absolute -bottom-20 -left-20 w-64 h-64 bg-blue-500/10 rounded-full animate-pulse-slower blur-3xl"></div>
    </div>

    <div class="w-full max-w-7xl mx-auto px-4 relative z-10 flex flex-col items-center justify-center">
      <!-- Section Header -->
      <div class="text-center mb-16 w-full flex flex-col items-center">
        <div class="inline-flex items-center bg-white/10 backdrop-blur-sm rounded-full px-6 py-3 mb-6 border border-white/20 justify-center">
          <div class="w-2 h-2 bg-blue-400 rounded-full mr-3 animate-pulse"></div>
          <span class="text-sm font-semibold text-white/80">📞 HABLEMOS DE TU PROYECTO</span>
        </div>

        <div class="h-5 w-full"></div>
        
        <h2 class="text-5xl md:text-6xl font-black mb-6 bg-gradient-to-r from-white via-blue-200 to-blue-100 bg-clip-text text-transparent text-center w-full">
          Comencemos Hoy
        </h2>
        <p class="text-xl text-white/80 max-w-3xl mx-auto leading-relaxed text-center">
          Contáctanos y recibe una cotización gratuita personalizada para tu proyecto. Transformemos tu idea en realidad.
        </p>
      </div>

      <div class="h-10 w-full"></div>
      
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 w-full max-w-6xl items-start">
        <!-- Contact Form -->
        <div class="bg-white/10 backdrop-blur-sm rounded-3xl p-8 border border-white/20 shadow-2xl w-full">
          <h3 class="text-3xl font-black text-white mb-12 text-center">Solicita Tu Cotización</h3>
          <div class="h-5 w-full"></div>
          <form class="space-y-6">
            <!-- Name & Email -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div class="group">
                <label class="block text-white/80 mb-3 font-semibold text-left">Nombre Completo</label>
                <input 
                  type="text" 
                  class="w-full px-5 py-4 bg-white/5 border border-white/20 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white placeholder-white/50 transition-all duration-300 group-hover:bg-white/10 text-left"
                  placeholder="Tu nombre"
                >
              </div>
              <div class="group">
                <label class="block text-white/80 mb-3 font-semibold text-left">Email</label>
                <input 
                  type="email" 
                  class="w-full px-5 py-4 bg-white/5 border border-white/20 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white placeholder-white/50 transition-all duration-300 group-hover:bg-white/10 text-left"
                  placeholder="tu@email.com"
                >
              </div>
            </div>
            
            <!-- Company -->
            <div class="group">
              <label class="block text-white/80 mb-3 font-semibold text-left">Empresa</label>
              <input 
                type="text" 
                class="w-full px-5 py-4 bg-white/5 border border-white/20 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white placeholder-white/50 transition-all duration-300 group-hover:bg-white/10 text-left"
                placeholder="Nombre de tu empresa"
              >
            </div>
            
            <!-- Service -->
            <div class="group">
              <label class="block text-white/80 mb-3 font-semibold text-left">Servicio de Interés</label>
              <select class="w-full px-5 py-4 bg-white/5 border border-white/20 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white transition-all duration-300 group-hover:bg-white/10 text-left">
                <option class="bg-blue-900 text-left">Selecciona un servicio</option>
                <option class="bg-blue-900 text-left">Plan Startup</option>
                <option class="bg-blue-900 text-left">Plan Growth</option>
                <option class="bg-blue-900 text-left">Plan Pro</option>
                <option class="bg-blue-900 text-left">Plan Enterprise</option>
                <option class="bg-blue-900 text-left">Desarrollo a medida</option>
              </select>
            </div>
            
            <!-- Message -->
            <div class="group">
              <label class="block text-white/80 mb-3 font-semibold text-left">Mensaje</label>
              <textarea 
                rows="5" 
                class="w-full px-5 py-4 bg-white/5 border border-white/20 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent text-white placeholder-white/50 transition-all duration-300 group-hover:bg-white/10 resize-none text-left"
                placeholder="Cuéntanos sobre tu proyecto, objetivos y cualquier requerimiento especial..."
              ></textarea>
            </div>
            <div class="h-5 w-full"></div>
            <!-- Submit Button -->
            <button 
              type="submit" 
              class="w-full bg-gradient-to-r from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 text-white font-black py-5 px-8 rounded-2xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 shadow-2xl hover:shadow-3xl text-lg relative overflow-hidden group"
            >
              <span class="relative z-10 flex items-center justify-center">
                Enviar Solicitud
                <span class="ml-3 transform transition-transform duration-500 group-hover:translate-x-1">🚀</span>
              </span>
              <div class="absolute inset-0 bg-white/20 transform -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
            </button>
          </form>
        </div>
        
        <!-- Contact Information -->
        <div class="flex flex-col justify-center space-y-8 items-start w-full">
          <!-- Contact Methods -->
          <div class="space-y-8 w-full">
            <!-- Phone -->
            <div class="flex items-start group cursor-pointer transform transition-all duration-500 hover:scale-105 w-full">
              <div class="w-16 h-16 bg-gradient-to-br from-blue-600 to-blue-800 rounded-2xl flex items-center justify-center mr-12 transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
                <span class="text-2xl">📞</span>
              </div>
              <div class="flex-1 text-left">
                <h4 class="text-xl font-black text-white mb-2">Teléfono</h4>
                <p class="text-blue-200 text-lg font-semibold">+54 9 11 5527-1430</p>
                <p class="text-white/60 text-sm">Lunes a Viernes 9:00 - 18:00</p>
              </div>
            </div>
            
            <!-- Email -->
            <div class="flex items-start group cursor-pointer transform transition-all duration-500 hover:scale-105 w-full">
              <div class="w-16 h-16 bg-gradient-to-br from-blue-700 to-blue-900 rounded-2xl flex items-center justify-center mr-12 transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
                <span class="text-2xl">✉️</span>
              </div>
              <div class="flex-1 text-left">
                <h4 class="text-xl font-black text-white mb-2">Email</h4>
                <p class="text-blue-200 text-lg font-semibold">contacto@jmgdesarrollos.com</p>
                <p class="text-white/60 text-sm">Respondemos en menos de 24 horas</p>
              </div>
            </div>
            
            <!-- Location -->
            <div class="flex items-start group cursor-pointer transform transition-all duration-500 hover:scale-105 w-full">
              <div class="w-16 h-16 bg-gradient-to-br from-blue-800 to-blue-950 rounded-2xl flex items-center justify-center mr-12 transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-6 shadow-lg">
                <span class="text-2xl">📍</span>
              </div>
              <div class="flex-1 text-left">
                <h4 class="text-xl font-black text-white mb-2">Ubicación</h4>
                <p class="text-blue-200 text-lg font-semibold">Buenos Aires, Argentina</p>
                <p class="text-white/60 text-sm">Trabajamos con clientes de todo el mundo</p>
              </div>
            </div>
          </div>

          <div class="h-10 w-full"></div>
          
          <!-- Quick Contact -->
          <div class="bg-gradient-to-br from-blue-600/20 to-blue-700/20 rounded-3xl p-8 border border-blue-500/30 backdrop-blur-sm w-full flex flex-col items-center text-center">
            <h4 class="text-2xl font-black text-white mb-4 text-center w-full">¿Necesitas una solución urgente?</h4>
            <p class="text-white/80 mb-6 text-center w-full max-w-md mx-auto">
              Contáctanos directamente por WhatsApp para una respuesta inmediata y atención personalizada.
            </p>
            <div class="h-5 w-full"></div>
            <button class="w-full max-w-xs bg-gradient-to-r from-green-500 to-blue-600 hover:from-green-600 hover:to-blue-700 text-white font-black py-4 px-6 rounded-2xl transition-all duration-500 transform hover:scale-105 shadow-lg hover:shadow-xl relative overflow-hidden group">
              <span class="relative z-10 flex items-center justify-center">
                💬 Chatear por WhatsApp
                <span class="ml-3 transform transition-transform duration-500 group-hover:translate-x-1">→</span>
              </span>
              <div class="absolute inset-0 bg-white/20 transform scale-x-0 group-hover:scale-x-100 transition-transform duration-500 origin-left"></div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Lógica del componente si es necesaria
</script>