<template>
  <section id="promo" class="py-16 bg-gradient-to-r from-amber-400 to-amber-600">
    <div class="max-w-7xl mx-auto px-4 text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-white mb-6">
        🎉 Promociones Especiales
      </h2>
      <p class="text-xl text-amber-100 mb-8 max-w-3xl mx-auto">
        Aprovecha nuestras ofertas limitadas para impulsar tu presencia digital
      </p>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
        <!-- Promo 1 -->
        <div class="bg-white rounded-2xl shadow-xl p-6 transform hover:scale-105 transition-transform duration-300">
          <div class="bg-red-500 text-white text-sm font-bold py-1 px-3 rounded-full inline-block mb-4">
            30% OFF
          </div>
          <h3 class="text-xl font-bold text-gray-800 mb-4">Sitio Web Básico</h3>
          <div class="text-3xl font-bold text-gray-800 mb-2">$299.999</div>
          <div class="text-lg text-gray-500 line-through mb-4">$428.570</div>
          <ul class="text-sm text-gray-600 space-y-2 mb-6">
            <li>✓ 5 páginas web</li>
            <li>✓ Diseño responsive</li>
            <li>✓ Formulario de contacto</li>
            <li>✓ SEO básico</li>
            <li>✓ Hosting por 1 año</li>
          </ul>
          <button class="w-full bg-amber-500 hover:bg-amber-600 text-white font-bold py-3 rounded-lg transition-colors duration-200">
            Obtener Oferta
          </button>
        </div>

        <!-- Promo 2 -->
        <div class="bg-white rounded-2xl shadow-xl p-6 transform hover:scale-105 transition-transform duration-300 border-4 border-amber-300 relative">
          <div class="absolute -top-4 left-1/2 transform -translate-x-1/2">
            <span class="bg-green-500 text-white text-sm font-bold py-1 px-4 rounded-full">
              MÁS POPULAR
            </span>
          </div>
          <div class="bg-green-500 text-white text-sm font-bold py-1 px-3 rounded-full inline-block mb-4">
            25% OFF
          </div>
          <h3 class="text-xl font-bold text-gray-800 mb-4">E-commerce Premium</h3>
          <div class="text-3xl font-bold text-gray-800 mb-2">$799.999</div>
          <div class="text-lg text-gray-500 line-through mb-4">$1.066.665</div>
          <ul class="text-sm text-gray-600 space-y-2 mb-6">
            <li>✓ Catálogo ilimitado</li>
            <li>✓ Carrito de compras</li>
            <li>✓ Pasarela de pagos</li>
            <li>✓ Panel administrativo</li>
            <li>✓ SSL y seguridad</li>
          </ul>
          <button class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-3 rounded-lg transition-colors duration-200">
            Obtener Oferta
          </button>
        </div>

        <!-- Promo 3 -->
        <div class="bg-white rounded-2xl shadow-xl p-6 transform hover:scale-105 transition-transform duration-300">
          <div class="bg-blue-500 text-white text-sm font-bold py-1 px-3 rounded-full inline-block mb-4">
            20% OFF
          </div>
          <h3 class="text-xl font-bold text-gray-800 mb-4">App Móvil</h3>
          <div class="text-3xl font-bold text-gray-800 mb-2">$1.199.999</div>
          <div class="text-lg text-gray-500 line-through mb-4">$1.499.999</div>
          <ul class="text-sm text-gray-600 space-y-2 mb-6">
            <li>✓ iOS y Android</li>
            <li>✓ Diseño nativo</li>
            <li>✓ Backend incluido</li>
            <li>✓ Publicación en stores</li>
            <li>✓ Soporte por 6 meses</li>
          </ul>
          <button class="w-full bg-blue-500 hover:bg-blue-600 text-white font-bold py-3 rounded-lg transition-colors duration-200">
            Obtener Oferta
          </button>
        </div>
      </div>
      
      <div class="mt-12 bg-white rounded-2xl p-6 max-w-4xl mx-auto">
        <h3 class="text-2xl font-bold text-gray-800 mb-4">¿No encuentras lo que buscas?</h3>
        <p class="text-gray-600 mb-6">
          Contáctanos para una cotización personalizada según tus necesidades específicas.
        </p>
        <button class="bg-gray-800 hover:bg-black text-white font-bold py-3 px-8 rounded-lg transition-colors duration-200">
          Solicitar Cotización Personalizada
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
// Lógica del componente si es necesaria
</script>