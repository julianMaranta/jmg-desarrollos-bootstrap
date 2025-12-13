<template>
  <section class="py-5 bg-light position-relative overflow-hidden w-100 d-flex justify-content-center">
    <!-- Background Elements -->
    <div class="position-absolute top-0 start-0 w-100 h-100 overflow-hidden">
      <div class="position-absolute top-0 end-0 bg-primary bg-opacity-5 rounded-circle animate-float-delayed blur-3" 
           style="width: 384px; height: 384px;"></div>
      <div class="position-absolute bottom-0 start-0 bg-primary bg-opacity-5 rounded-circle animate-float blur-3"
           style="width: 384px; height: 384px;"></div>
    </div>

    <div class="container position-relative z-3 d-flex flex-column align-items-center">
      <!-- Section Header -->
      <div class="text-center mb-5 w-100 d-flex flex-column align-items-center">
        <!-- MÁS ESPACIO DEBAJO DE "🎯 POR QUÉ ELEGIRNOS" -->
        <div class="d-inline-flex align-items-center bg-white bg-opacity-80 rounded-pill px-4 py-2 mb-5 border border-primary border-opacity-20 shadow">
          <div class="bg-primary rounded-circle me-2 animate-pulse" style="width: 8px; height: 8px;"></div>
          <span class="small fw-semibold text-secondary">🎯 POR QUÉ ELEGIRNOS</span>
        </div>

        <!-- ESPACIO EXTRA ANTES DEL TÍTULO -->
        <div class="h-3 w-100"></div>
        
        <h2 class="display-4 fw-black mb-4 text-primary text-center w-100">
          Ventajas Exclusivas
        </h2>
        <!-- ESPACIO AUMENTADO DEBAJO DEL TÍTULO -->
        <p class="h5 text-secondary mx-auto lead text-center mb-5">
          No solo desarrollamos sitios web, creamos <span class="fw-semibold text-primary">experiencias digitales</span> que impulsan tu negocio
        </p>
      </div>

      <!-- ESPACIO EXTRA ANTES DE FEATURES -->
      <div class="h-4 w-100"></div>

      <!-- Features Grid -->
      <div class="row g-4 mb-5 w-100 justify-content-center">
        <div v-for="(feature, index) in features" :key="index" 
             class="col-12 col-md-6 col-lg-3 d-flex justify-content-center">
          <div class="group text-center p-4 bg-white bg-opacity-80 rounded-4 shadow-lg transition-all duration-500 border border-primary border-opacity-25 w-100 d-flex flex-column align-items-center"
               style="max-width: 320px; backdrop-filter: blur(4px);">
            <!-- Icon Container -->
            <div class="position-relative mb-4 d-flex justify-content-center">
              <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center transition-all duration-500 group-hover-scale-rotate"
                   style="width: 80px; height: 80px;">
                <span class="text-white fs-3 d-flex align-items-center justify-content-center w-100 h-100">{{ feature.icon }}</span>
              </div>
              <div class="position-absolute top-n2 start-n2 w-100 h-100 bg-primary bg-opacity-20 rounded-3 blur-2 opacity-0 transition-opacity duration-500 group-hover-opacity"></div>
            </div>
            
            <!-- Content -->
            <h3 class="h4 fw-black text-dark mb-3 text-center">{{ feature.title }}</h3>
            <p class="text-secondary lh-base text-center flex-grow-1">
              {{ feature.description }}
            </p>
            
            <!-- Hover Effect Line -->
            <div class="w-0 h-1 bg-primary rounded-pill mt-4 transition-all duration-500 group-hover-line"></div>
          </div>
        </div>
      </div>

      <!-- ESPACIO EXTRA ANTES DE TECHNOLOGY & PROMISE -->
      <div class="h-5 w-100"></div>

      <!-- Technology & Promise Section -->
      <div class="row g-5 align-items-center w-100">
        <!-- Technology Stack -->
        <div class="col-12 col-lg-6 text-center text-lg-start d-flex flex-column align-items-center align-items-lg-start">
          <h3 class="display-5 fw-black text-dark mb-4 text-center w-100">
            Tecnología de Vanguardia
          </h3>
          <p class="fs-5 text-secondary mb-4 lh-base text-center text-lg-start w-100">
            Utilizamos el stack tecnológico más moderno para garantizar que tu sitio web sea 
            <span class="fw-semibold text-primary">rápido, seguro y escalable</span>.
          </p>
          
          <div class="row g-3 w-100">
            <div v-for="(tech, index) in technologies" :key="index" 
                 class="col-6 d-flex justify-content-center">
              <div class="d-flex align-items-center p-3 bg-white bg-opacity-50 rounded-3 shadow transition-all duration-300 group hover-scale w-100"
                   style="max-width: 280px;">
                <div class="bg-primary rounded-3 d-flex align-items-center justify-content-center me-3 transition-all duration-300 group-hover-rotate"
                     style="width: 48px; height: 48px;">
                  <span class="text-white fw-bold small d-flex align-items-center justify-content-center w-100 h-100">{{ tech.icon }}</span>
                </div>
                <div class="text-center text-lg-start">
                  <div class="fw-black text-dark">{{ tech.name }}</div>
                  <div class="small text-secondary">{{ tech.description }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Our Promise -->
        <div class="col-12 col-lg-6 d-flex justify-content-center mt-4">
          <div class="bg-primary rounded-4 p-4 text-white shadow-lg position-relative overflow-hidden w-100"
               style="max-width: 480px;">
            <!-- Background Pattern -->
            <div class="position-absolute top-0 start-0 w-100 h-100 opacity-10">
              <div class="w-100 h-100" style="background-image: radial-gradient(circle, white 1px, transparent 1px); background-size: 20px 20px;"></div>
            </div>
            
            <div class="position-relative z-2">
              <h4 class="h2 fw-black mb-4 text-center w-100">Nuestra Promesa</h4>
              <div class="h-3 w-100"></div>
              <div class="d-flex flex-column gap-4">
                <div v-for="(promise, index) in promises" :key="index" 
                     class="d-flex align-items-center p-3 bg-white bg-opacity-10 rounded-3 transition-all duration-300 hover-scale group justify-content-center justify-content-lg-start">
                  <div class="bg-white bg-opacity-20 rounded-3 d-flex align-items-center justify-content-center me-3 transition-all duration-300 group-hover-rotate"
                       style="width: 48px; height: 48px;">
                    <span class="text-white fs-5 d-flex align-items-center justify-content-center w-100 h-100">✓</span>
                  </div>
                  <div class="text-center text-lg-start">
                    <div class="fw-bold fs-6">{{ promise.title }}</div>
                    <div class="text-white text-opacity-80 small">{{ promise.description }}</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="h-5 w-100"></div>

      <!-- CTA Section -->
      <div class="text-center w-100 d-flex flex-column align-items-center justify-content-center">
        <div class="bg-primary bg-opacity-10 rounded-4 p-5 border border-primary border-opacity-20 w-100"
             style="max-width: 800px;">
          <div class="d-flex flex-column align-items-center justify-content-center gap-4">
            <h3 class="h1 fw-black text-dark text-center w-100">
              ¿Listo para Transformar tu Presencia Digital?
            </h3>
            <p class="fs-5 text-secondary mx-auto text-center">
              Únete a más de 200 empresas que ya confían en nosotros para llevar su negocio al siguiente nivel.
            </p>
            <div class="h-3 w-100"></div>
            <button 
              @click="scrollToSection('contacto')"
              class="btn btn-primary btn-lg fw-black py-3 px-5 rounded-3 transition-all duration-500 border-0 position-relative overflow-hidden"
            >
              <span class="position-relative z-2 d-flex align-items-center justify-content-center">
                Comenzar Proyecto
                <span class="ms-2 transition-all duration-500 group-hover-translate">🚀</span>
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

<style scoped>
/* Estilos personalizados para mantener las animaciones y efectos */
.top-n2 {
  top: -0.5rem;
}

.start-n2 {
  left: -0.5rem;
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
.blur-2 {
  filter: blur(8px);
}

.blur-3 {
  filter: blur(12px);
}

/* Efectos hover personalizados */
.group:hover .group-hover-scale-rotate {
  transform: scale(1.1) rotate(6deg);
}

.group:hover .group-hover-opacity {
  opacity: 1 !important;
}

.group:hover .group-hover-line {
  width: 4rem !important;
}

.group:hover .hover-scale {
  transform: scale(1.05);
}

.group:hover .group-hover-rotate {
  transform: rotate(12deg);
}

.group:hover .group-hover-translate {
  transform: translateX(0.5rem);
}

/* Utilidades de transición */
.transition-all {
  transition: all 0.3s ease;
}

.duration-300 {
  transition-duration: 300ms;
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

/* Utilidades de backdrop */
.bg-opacity-80 {
  --bs-bg-opacity: 0.8;
}

.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .display-4 {
    font-size: 2.5rem !important;
  }
  
  .display-5 {
    font-size: 2rem !important;
  }
  
  .h1 {
    font-size: 2rem !important;
  }
}

/* Asegurar altura consistente en las tarjetas de features */
.d-flex.flex-column {
  min-height: 100%;
}

.flex-grow-1 {
  flex-grow: 1;
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
</style>