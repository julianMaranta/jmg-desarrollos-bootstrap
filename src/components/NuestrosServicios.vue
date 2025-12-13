<template>
  <section id="servicios" class="services-modern">
    <!-- Fondo con gradiente animado -->
    <div class="background-animation">
      <div class="gradient-orbit orbit-1"></div>
      <div class="gradient-orbit orbit-2"></div>
      <div class="gradient-orbit orbit-3"></div>
      <div class="particle-field"></div>
    </div>

    <div class="container">
      <!-- Encabezado -->
      <div class="section-header">
        <div class="badge-modern">
          <div class="pulse-dot"></div>
          <span>✨ SERVICIOS PREMIUM</span>
        </div>
        <h1 class="title-modern">
          <span class="title-gradient">Soluciones Digitales</span>
          <span class="title-subtle">que impulsan tu negocio</span>
        </h1>
        <p class="subtitle-modern">
          Descubre nuestros planes diseñados para transformar tu presencia digital
        </p>
      </div>

      <!-- Grid de Planes -->
      <div class="plans-grid">
        
        <!-- Plan Essential -->
        <div class="plan-card essential">
          <div class="card-glow"></div>
          <div class="card-content">
            <div class="plan-header">
              <div class="plan-icon">
                <div class="icon-bg"></div>
                <span>🌱</span>
              </div>
              <div class="plan-title">
                <h3>Essential</h3>
                <p>Para empezar con fuerza</p>
              </div>
            </div>

            <div class="plan-price">
              <div class="price">$400.000</div>
              <div class="price-note">Hosting 1 año incluido</div>
            </div>

            <div class="plan-features">
              <div v-for="(feature, index) in basicFeatures" :key="index" class="feature-item">
                <div class="feature-check">
                  <svg width="16" height="16" viewBox="0 0 16 16">
                    <path d="M13.5 4.5L6 12L2.5 8.5" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
                  </svg>
                </div>
                <span>{{ feature }}</span>
              </div>
            </div>

            <button class="cta-button">
              <span>Iniciar Proyecto</span>
              <div class="button-arrow">
                <svg width="16" height="16" viewBox="0 0 16 16">
                  <path d="M8 0L16 8L8 16L6.5 14.5L12.5 8.5H0V7.5H12.5L6.5 1.5L8 0Z" fill="currentColor"/>
                </svg>
              </div>
            </button>
          </div>
        </div>

        <!-- Plan Growth (Destacado) -->
        <div class="plan-card growth featured">
          <div class="featured-badge">
            <span>🔥 MÁS POPULAR</span>
          </div>
          <div class="card-glow"></div>
          <div class="card-content">
            <div class="plan-header">
              <div class="plan-icon">
                <div class="icon-bg"></div>
                <span>🚀</span>
              </div>
              <div class="plan-title">
                <h3>Growth</h3>
                <p>Expansión acelerada</p>
              </div>
            </div>

            <div class="plan-price">
              <div class="price">$800.000</div>
              <div class="price-note">SEO Avanzado incluido</div>
            </div>

            <div class="plan-features">
              <div v-for="(feature, index) in standardFeatures" :key="index" class="feature-item">
                <div class="feature-check">
                  <svg width="16" height="16" viewBox="0 0 16 16">
                    <path d="M13.5 4.5L6 12L2.5 8.5" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
                  </svg>
                </div>
                <span>{{ feature }}</span>
              </div>
            </div>

            <button class="cta-button primary">
              <span>Seleccionar Plan</span>
              <div class="button-arrow">
                <svg width="16" height="16" viewBox="0 0 16 16">
                  <path d="M8 0L16 8L8 16L6.5 14.5L12.5 8.5H0V7.5H12.5L6.5 1.5L8 0Z" fill="currentColor"/>
                </svg>
              </div>
            </button>
          </div>
        </div>

        <!-- Plan Pro -->
        <div class="plan-card pro">
          <div class="card-glow"></div>
          <div class="card-content">
            <div class="plan-header">
              <div class="plan-icon">
                <div class="icon-bg"></div>
                <span>⭐</span>
              </div>
              <div class="plan-title">
                <h3>Pro</h3>
                <p>Máximo rendimiento</p>
              </div>
            </div>

            <div class="plan-price">
              <div class="price">$1.400.000</div>
              <div class="price-note">Gestión de datos incluida</div>
            </div>

            <div class="plan-features">
              <div v-for="(feature, index) in professionalFeatures" :key="index" class="feature-item">
                <div class="feature-check">
                  <svg width="16" height="16" viewBox="0 0 16 16">
                    <path d="M13.5 4.5L6 12L2.5 8.5" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
                  </svg>
                </div>
                <span>{{ feature }}</span>
              </div>
            </div>

            <button class="cta-button">
              <span>Ir Pro</span>
              <div class="button-arrow">
                <svg width="16" height="16" viewBox="0 0 16 16">
                  <path d="M8 0L16 8L8 16L6.5 14.5L12.5 8.5H0V7.5H12.5L6.5 1.5L8 0Z" fill="currentColor"/>
                </svg>
              </div>
            </button>
          </div>
        </div>

        <!-- Plan Enterprise -->
        <div class="plan-card enterprise">
          <div class="card-glow"></div>
          <div class="card-content">
            <div class="plan-header">
              <div class="plan-icon">
                <div class="icon-bg"></div>
                <span>🏢</span>
              </div>
              <div class="plan-title">
                <h3>Enterprise</h3>
                <p>Soluciones corporativas</p>
              </div>
            </div>

            <div class="plan-price">
              <div class="price">Personalizado</div>
              <div class="price-note">Aplicaciones Web & Mobile</div>
            </div>

            <div class="plan-features">
              <div v-for="(feature, index) in enterpriseFeatures" :key="index" class="feature-item">
                <div class="feature-check">
                  <svg width="16" height="16" viewBox="0 0 16 16">
                    <path d="M13.5 4.5L6 12L2.5 8.5" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
                  </svg>
                </div>
                <span>{{ feature }}</span>
              </div>
            </div>

            <button class="cta-button dark">
              <span>Contactar</span>
              <div class="button-arrow">
                <svg width="16" height="16" viewBox="0 0 16 16">
                  <path d="M8 0L16 8L8 16L6.5 14.5L12.5 8.5H0V7.5H12.5L6.5 1.5L8 0Z" fill="currentColor"/>
                </svg>
              </div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const basicFeatures = [
  'Página web con 5 secciones',
  'Diseño responsive avanzado',
  'SEO básico optimizado',
  'Hosting premium 1 año incluido',
  'Certificado SSL gratuito'
];

const standardFeatures = [
  'Animaciones avanzadas',
  'Diseño UX/UI exclusivo',
  'SEO avanzado integrado',
  'Formularios de contacto inteligentes',
  'Videos e imágenes optimizadas'
];

const professionalFeatures = [
  'Diseño premium personalizado',
  'Branding completo',
  'Panel de Administrador avanzado',
  'Contenido completamente editable',
  'Soporte prioritario 24/7'
];

const enterpriseFeatures = [
  'Desarrollo 100% a medida',
  'Consultoría estratégica digital',
  'Front-End + Back-End avanzado',
  'Soporte prioritario dedicado',
  'Backup y seguridad garantizados',
  'Infraestructura escalable'
];
</script>

<style scoped>
/* Variables CSS modernas */
:root {
  --primary: #6366f1;
  --primary-dark: #4f46e5;
  --primary-light: #8b5cf6;
  --dark: #1e293b;
  --light: #f8fafc;
  --gray: #64748b;
  --gray-light: #e2e8f0;
  --success: #10b981;
  --border-radius: 24px;
  --border-radius-sm: 16px;
  --shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 35px 60px -12px rgba(0, 0, 0, 0.15);
  --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Reset y base */
.services-modern {
  position: relative;
  min-height: 100vh;
  padding: 100px 0;
  background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
  overflow: hidden;
}

/* Animación de fondo */
.background-animation {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.gradient-orbit {
  position: absolute;
  border-radius: 50%;
  filter: blur(60px);
  opacity: 0.4;
  animation: orbit-float 20s ease-in-out infinite;
}

.orbit-1 {
  width: 400px;
  height: 400px;
  background: linear-gradient(135deg, var(--primary-light), var(--primary));
  top: 10%;
  left: 10%;
  animation-delay: 0s;
}

.orbit-2 {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, #10b981, #3b82f6);
  top: 60%;
  right: 10%;
  animation-delay: -7s;
}

.orbit-3 {
  width: 250px;
  height: 250px;
  background: linear-gradient(135deg, #f59e0b, #ef4444);
  bottom: 20%;
  left: 20%;
  animation-delay: -14s;
}

.particle-field {
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(circle at 25% 25%, rgba(99, 102, 241, 0.1) 2px, transparent 0),
    radial-gradient(circle at 75% 75%, rgba(79, 70, 229, 0.1) 2px, transparent 0);
  background-size: 50px 50px;
  animation: particle-move 20s linear infinite;
}

@keyframes orbit-float {
  0%, 100% {
    transform: translate(0, 0) scale(1);
  }
  25% {
    transform: translate(30px, -30px) scale(1.1);
  }
  50% {
    transform: translate(-20px, 20px) scale(0.9);
  }
  75% {
    transform: translate(-30px, -20px) scale(1.05);
  }
}

@keyframes particle-move {
  0% {
    background-position: 0 0, 0 0;
  }
  100% {
    background-position: 50px 50px, -50px -50px;
  }
}

/* Contenedor principal */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  position: relative;
  z-index: 2;
}

/* Encabezado de sección */
.section-header {
  text-align: center;
  margin-bottom: 80px;
}

.badge-modern {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 100px;
  padding: 8px 20px;
  margin-bottom: 30px;
  font-size: 14px;
  font-weight: 600;
  color: var(--gray);
  box-shadow: var(--shadow);
}

.pulse-dot {
  width: 8px;
  height: 8px;
  background: var(--primary);
  border-radius: 50%;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(1.2);
    opacity: 0.7;
  }
}

.title-modern {
  margin-bottom: 20px;
}

.title-gradient {
  display: block;
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 800;
  background: linear-gradient(135deg, var(--dark) 0%, var(--primary) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  line-height: 1.1;
}

.title-subtle {
  display: block;
  font-size: clamp(1.5rem, 3vw, 2rem);
  font-weight: 400;
  color: var(--gray);
  margin-top: 8px;
}

.subtitle-modern {
  font-size: 1.125rem;
  color: var(--gray);
  max-width: 500px;
  margin: 0 auto;
  line-height: 1.6;
}

/* Grid de planes */
.plans-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  align-items: start;
}

/* Tarjetas de planes */
.plan-card {
  position: relative;
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: var(--border-radius);
  padding: 30px;
  transition: var(--transition);
  box-shadow: var(--shadow);
  overflow: hidden;
}

.plan-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(99, 102, 241, 0.3), transparent);
}

.plan-card:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-lg);
  border-color: rgba(99, 102, 241, 0.2);
}

.plan-card.featured {
  border: 2px solid var(--primary);
  background: rgba(255, 255, 255, 0.9);
}

.featured-badge {
  position: absolute;
  top: -12px;
  left: 50%;
  transform: translateX(-50%);
  background: linear-gradient(135deg, var(--primary), var(--primary-light));
  color: white;
  padding: 8px 20px;
  border-radius: 100px;
  font-size: 12px;
  font-weight: 700;
  box-shadow: 0 10px 25px rgba(99, 102, 241, 0.3);
  z-index: 3;
}

.card-glow {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 50% 0%, rgba(99, 102, 241, 0.1), transparent 70%);
  opacity: 0;
  transition: var(--transition);
}

.plan-card:hover .card-glow {
  opacity: 1;
}

.card-content {
  position: relative;
  z-index: 2;
}

/* Header del plan */
.plan-header {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 25px;
}

.plan-icon {
  position: relative;
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon-bg {
  position: absolute;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, var(--primary-light), var(--primary));
  border-radius: 16px;
  opacity: 0.1;
  transition: var(--transition);
}

.plan-card:hover .icon-bg {
  opacity: 0.2;
  transform: scale(1.1);
}

.plan-icon span {
  font-size: 24px;
  z-index: 2;
}

.plan-title h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--dark);
  margin: 0 0 4px 0;
}

.plan-title p {
  font-size: 0.875rem;
  color: var(--gray);
  margin: 0;
}

/* Precio */
.plan-price {
  text-align: center;
  margin-bottom: 30px;
  padding: 20px 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.price {
  font-size: 2.5rem;
  font-weight: 800;
  color: var(--dark);
  margin-bottom: 8px;
  line-height: 1;
}

.price-note {
  font-size: 0.875rem;
  color: var(--gray);
  font-weight: 500;
}

/* Características */
.plan-features {
  margin-bottom: 30px;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 12px 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.03);
}

.feature-item:last-child {
  border-bottom: none;
}

.feature-check {
  width: 20px;
  height: 20px;
  background: var(--success);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  margin-top: 2px;
}

.feature-check svg {
  color: white;
}

.feature-item span {
  color: var(--dark);
  font-size: 0.9rem;
  line-height: 1.4;
  font-weight: 500;
}

/* Botones CTA */
.cta-button {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 16px 24px;
  background: rgba(99, 102, 241, 0.1);
  border: 1px solid rgba(99, 102, 241, 0.2);
  border-radius: var(--border-radius-sm);
  color: var(--primary);
  font-weight: 600;
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.cta-button::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
  transition: left 0.6s ease;
}

.cta-button:hover::before {
  left: 100%;
}

.cta-button:hover {
  background: var(--primary);
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(99, 102, 241, 0.3);
}

.cta-button.primary {
  background: var(--primary);
  color: white;
  border-color: var(--primary);
}

.cta-button.primary:hover {
  background: var(--primary-dark);
  transform: translateY(-2px);
  box-shadow: 0 15px 30px rgba(99, 102, 241, 0.4);
}

.cta-button.dark {
  background: var(--dark);
  color: white;
  border-color: var(--dark);
}

.cta-button.dark:hover {
  background: #0f172a;
  transform: translateY(-2px);
  box-shadow: 0 15px 30px rgba(30, 41, 59, 0.4);
}

.button-arrow {
  transition: transform 0.3s ease;
}

.cta-button:hover .button-arrow {
  transform: translateX(4px);
}

/* Responsive */
@media (max-width: 768px) {
  .services-modern {
    padding: 60px 0;
  }
  
  .plans-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .plan-card {
    padding: 25px 20px;
  }
  
  .section-header {
    margin-bottom: 50px;
  }
}

@media (max-width: 480px) {
  .plan-header {
    flex-direction: column;
    text-align: center;
    gap: 10px;
  }
  
  .plan-price {
    padding: 15px 0;
  }
  
  .price {
    font-size: 2rem;
  }
}
</style>