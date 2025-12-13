<template>
  <section id="proceso" class="py-5 bg-primary text-white position-relative overflow-hidden w-100 d-flex justify-content-center">
    <!-- Animated Background -->
    <div class="position-absolute top-0 start-0 w-100 h-100 overflow-hidden">
      <!-- Floating Particles -->
      <div v-for="i in 15" :key="i" 
           class="position-absolute rounded-circle bg-white bg-opacity-20 animate-float"
           :style="{
             left: Math.random() * 100 + '%',
             top: Math.random() * 100 + '%',
             animationDelay: Math.random() * 3 + 's',
             animationDuration: 2 + Math.random() * 2 + 's',
             width: '4px',
             height: '4px'
           }">
      </div>
      
      <!-- Gradient Orbs -->
      <div class="position-absolute top-0 start-0 bg-primary bg-opacity-10 rounded-circle animate-pulse-slow blur-3" 
           style="width: 320px; height: 320px; margin-top: -160px; margin-left: -160px;"></div>
      <div class="position-absolute bottom-0 end-0 bg-primary bg-opacity-10 rounded-circle animate-pulse-slower blur-3"
           style="width: 320px; height: 320px; margin-bottom: -160px; margin-right: -160px;"></div>
    </div>

    <div class="container position-relative z-3 d-flex flex-column align-items-center">
      <!-- Section Header -->
      <div class="text-center mb-5 w-100 d-flex flex-column align-items-center">
        <div class="d-inline-flex align-items-center bg-white bg-opacity-10 rounded-pill px-4 py-2 mb-4 border border-white border-opacity-20"
             style="backdrop-filter: blur(4px);">
          <div class="bg-info rounded-circle me-2 animate-pulse" style="width: 8px; height: 8px;"></div>
          <span class="small fw-semibold text-white text-opacity-80">🔄 NUESTRO PROCESO</span>
        </div>
        
        <div class="h-3 w-100"></div>

        <h2 class="display-4 fw-black mb-4 text-white text-center w-100">
          Metodología Probada
        </h2>
        
        <p class="h5 text-white text-opacity-80 mx-auto lead text-center">
          Un proceso estructurado que garantiza el éxito de tu proyecto desde el primer día hasta el lanzamiento
        </p>
      </div>

      <div class="h-4 w-100"></div>

      <!-- Process Timeline -->
      <div class="position-relative w-100">
        <!-- Timeline Line -->
        <div class="d-none d-lg-block position-absolute top-0 start-50 bottom-0 w-1 bg-primary bg-opacity-50 translate-middle-x"></div>
        
        <!-- Process Steps -->
        <div class="w-100">
          <!-- Step 1 -->
          <div class="d-flex flex-column flex-lg-row align-items-center align-items-lg-start gap-4 group w-100 mb-5">
            <!-- Content -->
            <div class="col-lg-6 order-2 order-lg-1 d-flex justify-content-center justify-content-lg-end">
              <div class="bg-white bg-opacity-10 rounded-4 p-4 border border-white border-opacity-20 shadow-lg transition-all duration-500 group-hover-scale w-100"
                   style="max-width: 500px; backdrop-filter: blur(4px);">
                <div class="d-flex align-items-center justify-content-center mb-4">
                  <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center text-white fw-black fs-2 shadow transition-all duration-500 group-hover-scale-rotate"
                       style="width: 64px; height: 64px;">
                    1
                  </div>
                </div>
                <h3 class="h2 fw-black text-white mb-3 text-center">Descubrimiento & Estrategia</h3>
                <p class="text-white text-opacity-80 lh-base fs-6 text-center">
                  Comprendemos profundamente tu negocio, objetivos y audiencia para crear una estrategia digital personalizada que impulse tus resultados.
                </p>
                <ul class="mt-4 list-unstyled">
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Análisis de competencia</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Definición de objetivos</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Planificación estratégica</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <!-- Visual -->
            <div class="col-lg-6 order-1 order-lg-2 d-flex justify-content-center justify-content-lg-start">
              <div class="bg-primary bg-opacity-20 rounded-4 d-flex align-items-center justify-content-center transition-all duration-500 group-hover-scale-rotate-3 shadow-lg border border-white border-opacity-10"
                   style="width: 192px; height: 192px;">
                <span class="fs-1">💡</span>
              </div>
            </div>
          </div>

          <div class="h-4 w-100"></div>

          <!-- Step 2 -->
          <div class="d-flex flex-column flex-lg-row align-items-center align-items-lg-start gap-4 group w-100 mb-5">
            <!-- Visual -->
            <div class="col-lg-6 order-1 d-flex justify-content-center justify-content-lg-end">
              <div class="bg-primary bg-opacity-25 rounded-4 d-flex align-items-center justify-content-center transition-all duration-500 group-hover-scale-rotate-3 shadow-lg border border-white border-opacity-10"
                   style="width: 192px; height: 192px;">
                <span class="fs-1">🎨</span>
              </div>
            </div>
            
            <!-- Content -->
            <div class="col-lg-6 order-2 d-flex justify-content-center justify-content-lg-start">
              <div class="bg-white bg-opacity-10 rounded-4 p-4 border border-white border-opacity-20 shadow-lg transition-all duration-500 group-hover-scale w-100"
                   style="max-width: 500px; backdrop-filter: blur(4px);">
                <div class="d-flex align-items-center justify-content-center mb-4">
                  <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center text-white fw-black fs-2 shadow transition-all duration-500 group-hover-scale-rotate"
                       style="width: 64px; height: 64px;">
                    2
                  </div>
                </div>
                <h3 class="h2 fw-black text-white mb-3 text-center">Diseño & Experiencia</h3>
                <p class="text-white text-opacity-80 lh-base fs-6 text-center">
                  Creamos diseños visualmente impactantes y experiencias de usuario fluidas que reflejan tu marca y optimizan la conversión.
                </p>
                <ul class="mt-4 list-unstyled">
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Wireframes y prototipos</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Diseño UI/UX personalizado</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Pruebas de usabilidad</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <div class="h-4 w-100"></div>

          <!-- Step 3 -->
          <div class="d-flex flex-column flex-lg-row align-items-center align-items-lg-start gap-4 group w-100 mb-5">
            <!-- Content -->
            <div class="col-lg-6 order-2 order-lg-1 d-flex justify-content-center justify-content-lg-end">
              <div class="bg-white bg-opacity-10 rounded-4 p-4 border border-white border-opacity-20 shadow-lg transition-all duration-500 group-hover-scale w-100"
                   style="max-width: 500px; backdrop-filter: blur(4px);">
                <div class="d-flex align-items-center justify-content-center mb-4">
                  <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center text-white fw-black fs-2 shadow transition-all duration-500 group-hover-scale-rotate"
                       style="width: 64px; height: 64px; background: linear-gradient(135deg, #0a58ca, #084298);">
                    3
                  </div>
                </div>
                <h3 class="h2 fw-black text-white mb-3 text-center">Desarrollo & Implementación</h3>
                <p class="text-white text-opacity-80 lh-base fs-6 text-center">
                  Programamos tu sitio web con las mejores tecnologías, asegurando máximo rendimiento, seguridad y escalabilidad para el futuro.
                </p>
                <ul class="mt-4 list-unstyled">
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Desarrollo frontend y backend</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Integración de funcionalidades</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Optimización SEO técnico</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <!-- Visual -->
            <div class="col-lg-6 order-1 order-lg-2 d-flex justify-content-center justify-content-lg-start">
              <div class="bg-primary bg-opacity-30 rounded-4 d-flex align-items-center justify-content-center transition-all duration-500 group-hover-scale-rotate-3 shadow-lg border border-white border-opacity-10"
                   style="width: 192px; height: 192px;">
                <span class="fs-1">⚡</span>
              </div>
            </div>
          </div>

          <div class="h-4 w-100"></div>

          <!-- Step 4 -->
          <div class="d-flex flex-column flex-lg-row align-items-center align-items-lg-start gap-4 group w-100 mb-5">
            <!-- Visual -->
            <div class="col-lg-6 order-1 d-flex justify-content-center justify-content-lg-end">
              <div class="bg-primary bg-opacity-35 rounded-4 d-flex align-items-center justify-content-center transition-all duration-500 group-hover-scale-rotate-3 shadow-lg border border-white border-opacity-10"
                   style="width: 192px; height: 192px;">
                <span class="fs-1">🚀</span>
              </div>
            </div>
            
            <!-- Content -->
            <div class="col-lg-6 order-2 d-flex justify-content-center justify-content-lg-start">
              <div class="bg-white bg-opacity-10 rounded-4 p-4 border border-white border-opacity-20 shadow-lg transition-all duration-500 group-hover-scale w-100"
                   style="max-width: 500px; backdrop-filter: blur(4px);">
                <div class="d-flex align-items-center justify-content-center mb-4">
                  <div class="bg-dark rounded-3 d-flex align-items-center justify-content-center text-white fw-black fs-2 shadow transition-all duration-500 group-hover-scale-rotate"
                       style="width: 64px; height: 64px;">
                    4
                  </div>
                </div>
                <h3 class="h2 fw-black text-white mb-3 text-center">Lanzamiento & Crecimiento</h3>
                <p class="text-white text-opacity-80 lh-base fs-6 text-center">
                  Desplegamos tu sitio web y proporcionamos soporte continuo para garantizar su éxito a largo plazo y crecimiento constante.
                </p>
                <ul class="mt-4 list-unstyled">
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Lanzamiento y deployment</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center mb-2">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Monitoreo y analytics</span>
                  </li>
                  <li class="d-flex align-items-center justify-content-center">
                    <div class="bg-info rounded-circle me-2" style="width: 8px; height: 8px;"></div>
                    <span class="text-white text-opacity-70">Soporte y mantenimiento</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="h-4 w-100"></div>

      <!-- CTA Section -->
      <div class="text-center mt-5 w-100 d-flex flex-column align-items-center justify-content-center">
        <div class="bg-primary bg-opacity-20 rounded-4 p-5 border border-primary border-opacity-30 w-100 mx-auto d-flex flex-column align-items-center justify-content-center"
             style="max-width: 800px;">
          <h3 class="h1 fw-black text-white mb-4 text-center w-100">
            ¿Listo para Iniciar tu Proyecto?
          </h3>
          <p class="fs-5 text-white text-opacity-80 mb-4 text-center">
            Sigue los pasos de más de 200 empresas exitosas que confiaron en nuestro proceso probado.
          </p>
          <div class="h-3 w-100"></div>
          <div class="d-flex justify-content-center w-100">
            <button 
              @click="scrollToSection('contacto')"
              class="btn btn-primary btn-lg fw-black py-3 px-5 rounded-3 transition-all duration-500 border-0 position-relative overflow-hidden"
            >
              <span class="position-relative z-2 d-flex align-items-center justify-content-center">
                Iniciar Proceso
                <span class="ms-2 transition-all duration-500 group-hover-translate">🎯</span>
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
.bg-gradient-custom {
  background: linear-gradient(135deg, #0a58ca, #0d6efd, #0a58ca);
}

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

.animate-pulse-slow {
  animation: pulse-slow 4s ease-in-out infinite;
}

.animate-pulse-slower {
  animation: pulse-slower 6s ease-in-out infinite;
}

.animate-pulse {
  animation: pulse-slow 2s ease-in-out infinite;
}

/* Efectos blur personalizados */
.blur-3 {
  filter: blur(12px);
}

/* Efectos hover personalizados */
.group:hover .group-hover-scale {
  transform: scale(1.05);
}

.group:hover .group-hover-scale-rotate {
  transform: scale(1.1) rotate(6deg);
}

.group:hover .group-hover-scale-rotate-3 {
  transform: scale(1.1) rotate(3deg);
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

.translate-middle-x {
  transform: translateX(-50%);
}

/* Bordes redondeados personalizados */
.rounded-4 {
  border-radius: 1rem;
}

/* Utilidades de backdrop */
.bg-opacity-10 {
  --bs-bg-opacity: 0.1;
}

.bg-opacity-20 {
  --bs-bg-opacity: 0.2;
}

.bg-opacity-25 {
  --bs-bg-opacity: 0.25;
}

.bg-opacity-30 {
  --bs-bg-opacity: 0.3;
}

.bg-opacity-35 {
  --bs-bg-opacity: 0.35;
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

/* Utilidades de opacidad */
.text-opacity-80 {
  --bs-text-opacity: 0.8;
}

.text-opacity-70 {
  --bs-text-opacity: 0.7;
}

/* Altura de línea mejorada */
.lh-base {
  line-height: 1.6;
}
</style>