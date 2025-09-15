<template>
  <!-- Hero Section -->
  <section id="hero" class="hero-section">
    <div class="hero-background"></div>
    <div class="floating-particles"></div>
    <div class="hero-content">
      <div class="location-badge animate-fade-in-up animate-delay-1">
        <span class="location-icon animate-float">
          <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M12.5 13.4271C14.2231 13.4271 15.62 12.0302 15.62 10.3071C15.62 8.58398 14.2231 7.1871 12.5 7.1871C10.7769 7.1871 9.38 8.58398 9.38 10.3071C9.38 12.0302 10.7769 13.4271 12.5 13.4271Z" stroke="white" stroke-width="1.5"/>
          <path d="M4.11971 8.4871C6.08971 -0.172897 18.9197 -0.162897 20.8797 8.4971C22.0297 13.5771 18.8697 17.8771 16.0997 20.5371C14.0897 22.4771 10.9097 22.4771 8.88971 20.5371C6.12971 17.8771 2.96971 13.5671 4.11971 8.4871Z" stroke="white" stroke-width="1.5"/>
          </svg>
        </span>
        {{ t('hero.location') }}
      </div>
      <h1 class="hero-title animate-fade-in-up animate-delay-2">{{ t('hero.title') }}</h1>
      <p class="hero-tagline animate-fade-in-up animate-delay-3">{{ t('hero.tagline') }}</p>
      <p class="hero-description animate-fade-in-up animate-delay-4">{{ t('hero.description') }}</p>
      <button class="cta-button btn-magnetic hover-lift animate-fade-in-up animate-delay-5" @click="scrollToSection('services')">
        {{ t('hero.cta') }} 
        <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M14.9297 5.92725L20.9997 11.9972L14.9297 18.0672" stroke="white" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
        <path d="M4 11.9971H20.83" stroke="white" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </button>
    </div>
    <div class="hero-footer animate-delay-5">
      <span class="established animate-pulse">{{ t('hero.established') }}</span>
    </div>
  </section>
</template>

<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()

const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ 
      behavior: 'smooth',
      block: 'start',
      inline: 'nearest'
    })
  }
}
</script>

<style scoped>
/* Hero Section Styles */
.hero-section {
  min-height: 100dvh;
  background-image: url('../assets/images/hero.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  padding-top: 80px;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: var(--color-bg-primary);
  opacity: 0.94;
}

.floating-particles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 1;
}

.floating-particles::before,
.floating-particles::after {
  content: '';
  position: absolute;
  width: 4px;
  height: 4px;
  background: var(--color-secondary);
  border-radius: 50%;
  animation: particle-float 6s infinite ease-in-out;
}

.floating-particles::before {
  left: 20%;
  animation-delay: 0s;
}

.floating-particles::after {
  left: 80%;
  animation-delay: 3s;
}

.hero-content {
  text-align: center;
  color: var(--color-text-primary);
  z-index: var(--z-content);
  max-width: 800px;
  padding: 0 var(--spacing-lg);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.location-badge {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  background: var(--color-bg-card);
  backdrop-filter: var(--backdrop-blur-xl);
  padding: 10px;
  border-radius: var(--radius-lg);
  margin-bottom: var(--spacing-lg);
  font-size: var(--text-xs);
}

.hero-title {
  font-size: var(--text-5xl);
  font-weight: var(--font-bold);
  margin-bottom: var(--spacing-sm);
  background-color: var(--color-text-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-tagline {
  font-size: var(--text-xl);
  margin-bottom: var(--spacing-sm);
  opacity: 0.9;
  color: var(--color-text-secondary);
}

.hero-description {
  font-size: var(--text-base);
  margin-bottom: var(--spacing-lg);
  opacity: 0.8;
  line-height: 1.6;
}

.cta-button {
  background: var(--gradient-primary);
  color: var(--color-text-primary);
  border: none;
  padding: 20px;
  border-radius: var(--radius-lg);
  font-size: var(--text-base);
  font-weight: var(--font-semibold);
  cursor: pointer;
  transition: transform var(--transition-fast), box-shadow var(--transition-fast);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-cta);
}

.hero-footer {
  position: absolute;
  bottom: var(--spacing-lg);
  left: 50%;
  transform: translateX(-50%);
  color: var(--color-accent);
  font-size: var(--text-xs);
}

/* RTL Support for Hero */
[dir="rtl"] .hero-content {
  text-align: center;
}

/* Responsive Design for Hero */
@media (max-width: 768px) {
  .hero-title {
    font-size: var(--text-3xl);
  }
  
  .hero-tagline {
    font-size: var(--text-lg);
  }
}
</style>
