<template>
  <section id="testimonios" class="py-5 bg-light position-relative overflow-hidden w-100 d-flex justify-content-center align-items-center">
    <!-- Background Elements -->
    <div class="position-absolute top-0 start-0 w-100 h-100 overflow-hidden">
      <div class="position-absolute top-0 end-0 bg-primary bg-opacity-5 rounded-circle animate-float-delayed blur-3" 
           style="width: 384px; height: 384px;"></div>
      <div class="position-absolute bottom-0 start-0 bg-primary bg-opacity-5 rounded-circle animate-float blur-3"
           style="width: 384px; height: 384px;"></div>
    </div>

    <div class="container position-relative z-3 d-flex flex-column align-items-center justify-content-center">
      <!-- Section Header -->
      <div class="text-center mb-5 w-100 d-flex flex-column align-items-center">
        <div class="d-inline-flex align-items-center bg-white bg-opacity-80 rounded-pill px-4 py-2 mb-4 border border-primary border-opacity-20 shadow justify-content-center"
             style="backdrop-filter: blur(4px);">
          <div class="bg-primary rounded-circle me-2 animate-pulse" style="width: 8px; height: 8px;"></div>
          <span class="small fw-semibold text-secondary">💬 LO QUE DICEN NUESTROS CLIENTES</span>
        </div>

        <div class="h-3 w-100"></div>
        
        <h2 class="display-4 fw-black mb-4 text-primary text-center w-100">
          Historias de Éxito
        </h2>
        <p class="h5 text-secondary mx-auto lead text-center">
          Más de 200 empresas confían en nosotros para transformar su presencia digital y alcanzar nuevos niveles de crecimiento
        </p>
      </div>

      <div class="h-4 w-100"></div>

      <!-- Testimonials Grid -->
      <div class="row g-4 mb-5 w-100 justify-content-center">
        <!-- Testimonio 1 -->
        <div class="col-12 col-md-6 col-lg-4 d-flex justify-content-center">
          <div class="group bg-white bg-opacity-80 rounded-4 p-4 shadow-lg transition-all duration-500 border border-primary border-opacity-25 w-100 d-flex flex-column align-items-center text-center"
               style="max-width: 380px; backdrop-filter: blur(4px);">
            <!-- Header -->
            <div class="d-flex flex-column align-items-center mb-4 w-100">
              <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center mb-3 transition-all duration-500 group-hover-scale-rotate"
                   style="width: 64px; height: 64px;">
                <span class="text-white fw-bold fs-5">MR</span>
              </div>
              <div class="text-center w-100">
                <h4 class="fw-black text-dark fs-5">María Rodríguez</h4>
                <p class="text-secondary small">Dueña de Boutique Elegante</p>
              </div>
            </div>
            
            <!-- Rating -->
            <div class="d-flex mb-3 justify-content-center w-100">
              <span v-for="star in 5" :key="star" class="text-warning fs-6">⭐</span>
            </div>
            
            <!-- Testimonial Text -->
            <p class="text-secondary lh-base fst-italic mb-4 w-100 text-center">
              "JMG Desarrollos transformó completamente mi negocio. Mi sitio web no solo es hermoso, sino que ha aumentado mis ventas online en un 300%. El equipo es profesional y muy comprometido con el éxito del proyecto."
            </p>
            
            <!-- Results -->
            <div class="bg-primary bg-opacity-10 rounded-3 p-3 border border-primary border-opacity-25 w-100">
              <div class="d-flex justify-content-between align-items-center small">
                <span class="text-primary fw-semibold">Resultados:</span>
                <span class="text-success fw-black">+300% Ventas</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonio 2 -->
        <div class="col-12 col-md-6 col-lg-4 d-flex justify-content-center">
          <div class="group bg-white bg-opacity-80 rounded-4 p-4 shadow-lg transition-all duration-500 border border-primary border-opacity-25 w-100 d-flex flex-column align-items-center text-center"
               style="max-width: 380px; backdrop-filter: blur(4px);">
            <!-- Header -->
            <div class="d-flex flex-column align-items-center mb-4 w-100">
              <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center mb-3 transition-all duration-500 group-hover-scale-rotate"
                   style="width: 64px; height: 64px; background: linear-gradient(135deg, #0a58ca, #084298);">
                <span class="text-white fw-bold fs-5">CP</span>
              </div>
              <div class="text-center w-100">
                <h4 class="fw-black text-dark fs-5">Carlos Pérez</h4>
                <p class="text-secondary small">Director de TechSolutions</p>
              </div>
            </div>
            
            <!-- Rating -->
            <div class="d-flex mb-3 justify-content-center w-100">
              <span v-for="star in 5" :key="star" class="text-warning fs-6">⭐</span>
            </div>
            
            <!-- Testimonial Text -->
            <p class="text-secondary lh-base fst-italic mb-4 w-100 text-center">
              "Trabajamos con JMG para nuestro sitio corporativo y los resultados superaron expectativas. El proceso fue transparente, la comunicación excelente y la entrega fue puntual. Definitivamente los recomiendo."
            </p>
            
            <!-- Results -->
            <div class="bg-primary bg-opacity-15 rounded-3 p-3 border border-primary border-opacity-50 w-100">
              <div class="d-flex justify-content-between align-items-center small">
                <span class="text-primary fw-semibold">Resultados:</span>
                <span class="text-success fw-black">+150% Leads</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonio 3 -->
        <div class="col-12 col-md-6 col-lg-4 d-flex justify-content-center">
          <div class="group bg-white bg-opacity-80 rounded-4 p-4 shadow-lg transition-all duration-500 border border-primary border-opacity-25 w-100 d-flex flex-column align-items-center text-center"
               style="max-width: 380px; backdrop-filter: blur(4px);">
            <!-- Header -->
            <div class="d-flex flex-column align-items-center mb-4 w-100">
              <div class="bg-dark rounded-3 d-flex align-items-center justify-content-center mb-3 transition-all duration-500 group-hover-scale-rotate"
                   style="width: 64px; height: 64px;">
                <span class="text-white fw-bold fs-5">AG</span>
              </div>
              <div class="text-center w-100">
                <h4 class="fw-black text-dark fs-5">Ana García</h4>
                <p class="text-secondary small">Fundadora de Wellness Center</p>
              </div>
            </div>
            
            <!-- Rating -->
            <div class="d-flex mb-3 justify-content-center w-100">
              <span v-for="star in 5" :key="star" class="text-warning fs-6">⭐</span>
            </div>
            
            <!-- Testimonial Text -->
            <p class="text-secondary lh-base fst-italic mb-4 w-100 text-center">
              "Increíble experiencia de principio a fin. Mi sitio web captura perfectamente la esencia de mi marca y ha sido clave para atraer nuevos clientes. El soporte post-venta es excepcional y siempre están disponibles."
            </p>
            
            <!-- Results -->
            <div class="bg-primary bg-opacity-20 rounded-3 p-3 border border-primary border-opacity-75 w-100">
              <div class="d-flex justify-content-between align-items-center small">
                <span class="text-primary fw-semibold">Resultados:</span>
                <span class="text-success fw-black">+200% Clientes</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="h-4 w-100"></div>

      <!-- Client Logos -->
      <div class="text-center w-100 d-flex flex-column align-items-center">
        <h3 class="h2 fw-black text-dark mb-4 text-center w-100">
          Empresas que Confían en Nosotros
        </h3>
        <div class="h-3 w-100"></div>
        <div class="row g-4 align-items-center w-100 opacity-75 justify-content-center">
          <div v-for="i in 6" :key="i" 
               class="col-6 col-md-4 col-lg-2 d-flex justify-content-center">
            <div class="bg-white bg-opacity-80 rounded-3 d-flex flex-column align-items-center justify-content-center shadow transition-all duration-500 hover-scale group border border-primary border-opacity-25 w-100"
                 style="height: 96px; backdrop-filter: blur(4px); max-width: 160px;">
              <div class="text-center w-100 d-flex flex-column align-items-center justify-content-center">
                <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center mb-1 transition-all duration-500 group-hover-rotate"
                     style="width: 40px; height: 40px;">
                  <span class="text-white fw-bold small d-flex align-items-center justify-content-center w-100">C{{ i }}</span>
                </div>
                <span class="text-secondary fw-semibold small text-center w-100">Cliente {{ i }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="h-4 w-100"></div>

      <!-- CTA Section -->
      <div class="text-center mt-5 w-100">
        <div class="bg-primary bg-opacity-10 rounded-4 p-5 border border-primary border-opacity-20 w-100 d-flex flex-column align-items-center justify-content-center">
          <h3 class="h1 fw-black text-dark mb-4 text-center w-100">
            ¿Listo para ser Nuestro Próximo Caso de Éxito?
          </h3>
          
          <div class="d-flex align-items-center justify-content-center w-100 mb-4">
            <p class="fs-5 text-secondary text-center lh-base">
              Únete a las empresas que ya experimentaron la transformación digital con JMG Desarrollos.
            </p>
          </div>

          <div class="h-3 w-100"></div>

          <div class="d-flex justify-content-center w-100">
            <button 
              @click="scrollToSection('contacto')"
              class="btn btn-primary btn-lg fw-black py-3 px-5 rounded-3 transition-all duration-500 border-0 position-relative overflow-hidden"
            >
              <span class="position-relative z-2 d-flex align-items-center justify-content-center">
                Unirme al Éxito
                <span class="ms-2 transition-all duration-500 group-hover-translate">🎉</span>
              </span>
              <div class="position-absolute top-0 start-0 w-100 h-100 bg-white bg-opacity-20 skew-x-12 translate-x-n100 transition-transform duration-1000"></div>
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

@keyframes pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}

.animate-float {
  animation: float 4s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float-delayed 5s ease-in-out infinite;
}

.animate-pulse {
  animation: pulse 2s ease-in-out infinite;
}

/* Efectos blur personalizados */
.blur-3 {
  filter: blur(12px);
}

/* Efectos hover personalizados */
.group:hover .group-hover-scale-rotate {
  transform: scale(1.1) rotate(6deg);
}

.group:hover .group-hover-rotate {
  transform: rotate(12deg);
}

.group:hover .hover-scale {
  transform: scale(1.1);
}

.group:hover .group-hover-translate {
  transform: translateX(0.5rem);
}

/* Utilidades de transición */
.transition-all {
  transition: all 0.3s ease;
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
.bg-opacity-80 {
  --bs-bg-opacity: 0.8;
}

.bg-opacity-10 {
  --bs-bg-opacity: 0.1;
}

.bg-opacity-15 {
  --bs-bg-opacity: 0.15;
}

.bg-opacity-20 {
  --bs-bg-opacity: 0.2;
}

.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .display-4 {
    font-size: 2.5rem !important;
  }
  
  .h1 {
    font-size: 2rem !important;
  }
  
  .h2 {
    font-size: 1.75rem !important;
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
}

/* Efectos de hover para botones */
.btn:hover .translate-x-n100 {
  transform: translateX(100%) skewX(-12deg) !important;
}

/* Altura de línea mejorada */
.lh-base {
  line-height: 1.6;
}

/* Opacidad para logos de clientes */
.opacity-75 {
  opacity: 0.75;
}

/* Efecto de elevación en hover para tarjetas */
.group:hover {
  transform: translateY(-1rem);
}
</style>