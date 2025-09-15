<template>
  <!-- Navigation -->
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-logo">
        <img src="../assets/logo.svg" alt="IltizamTech Logo" class="nav-logo-img">
        <span class="logo-text">{{ t('nav.companyName') }}</span>
      </div>
      <div class="nav-links">
        <a href="#about" @click="scrollToSection('about')">{{ t('nav.about') }}</a>
        <a href="#services" @click="scrollToSection('services')">{{ t('nav.services') }}</a>
        <a href="#projects" @click="scrollToSection('projects')">{{ t('nav.projects') }}</a>
        <a href="#contact" @click="scrollToSection('contact')">{{ t('nav.contact') }}</a>
      </div>
      <div class="nav-actions">
        <div class="lang-dropdown">
            <button @click="toggleDropdown" class="lang-btn hover-lift">
              <span class="lang-text">{{ currentLocale === 'en' ? 'EN' : 'AR' }}</span>
              <span class="dropdown-arrow" :class="{ 'rotated': showDropdown }">▼</span>
            </button>
          <div v-if="showDropdown" class="lang-options">
            <button @click="selectLanguage('en')" :class="{ active: currentLocale === 'en' }" class="lang-option hover-bounce">
              EN
            </button>
            <button @click="selectLanguage('ar')" :class="{ active: currentLocale === 'ar' }" class="lang-option hover-bounce">
              AR
            </button>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { useI18n } from 'vue-i18n'

const { locale, t } = useI18n()
const currentLocale = ref('en')
const showDropdown = ref(false)

const loadLanguageFromStorage = () => {
  const savedLang = localStorage.getItem('iltizamtech-language')
  if (savedLang && (savedLang === 'en' || savedLang === 'ar')) {
    currentLocale.value = savedLang
    locale.value = savedLang
    document.documentElement.dir = savedLang === 'ar' ? 'rtl' : 'ltr'
    document.documentElement.lang = savedLang
  }
}

const toggleDropdown = () => {
  showDropdown.value = !showDropdown.value
}

const selectLanguage = (lang: string) => {
  currentLocale.value = lang
  locale.value = lang
  document.documentElement.dir = lang === 'ar' ? 'rtl' : 'ltr'
  document.documentElement.lang = lang
  showDropdown.value = false
  
  localStorage.setItem('iltizamtech-language', lang)
}

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

onMounted(() => {
  loadLanguageFromStorage()
})
</script>

<style scoped>
/* Navigation Styles */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: var(--z-navbar);
  background: var(--color-bg-overlay);
  backdrop-filter: var(--backdrop-blur-lg);
  padding: var(--spacing-sm) 0;
  border: none;
  margin: 0;
}

.nav-container {
  padding: 0 var(--spacing-lg);
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.nav-logo-img {
  width: 60px;
  height: 60px;
}

.logo-text {
  color: var(--color-text-primary);
  font-weight: var(--font-bold);
  font-size: var(--text-xl);
}

.nav-links {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: var(--spacing-lg);
}

.nav-links a {
  color: var(--color-text-primary);
  text-decoration: none;
  font-weight: var(--font-medium);
  transition: color var(--transition-fast);
  font-size: var(--text-xl);
}

.nav-links a:hover {
  color: var(--color-secondary);
}

.nav-actions {
  padding-inline: 0.5rem;
}

/* Language Dropdown */
.lang-dropdown {
  position: relative;
  display: inline-block;
}

.lang-btn {
  background: var(--color-text-primary);
  border: 1px solid rgba(255, 255, 255, 0.2);
  color: var(--color-bg-primary);
  padding: var(--spacing-xs) var(--spacing-sm);
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: all var(--transition-fast);
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
  font-weight: var(--font-semibold);
}

.lang-btn:hover {
  background: var(--color-text-secondary);
}

.lang-text {
  transition: all var(--transition-fast);
}

.dropdown-arrow {
  transition: transform var(--transition-fast);
  font-size: 0.8em;
}

.dropdown-arrow.rotated {
  transform: rotate(180deg);
}

.lang-options {
  position: absolute;
  top: 100%;
  right: 0;
  background: var(--color-text-primary);
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: var(--radius-sm);
  width: 100%;
  z-index: var(--z-dropdown);
  margin-top: var(--spacing-xs);
  box-shadow: var(--shadow-card);
}

.lang-option {
  background: none;
  border: none;
  color: var(--color-bg-primary);
  padding: var(--spacing-xs) var(--spacing-sm);
  cursor: pointer;
  transition: all var(--transition-fast);
  font-size: var(--text-xs);
  font-weight: var(--font-semibold);
  width: 100%;
  text-align: center;
  display: block;
  box-sizing: border-box;
}

.lang-option:hover {
  background: var(--color-bg-overlay);
}

.lang-option.active {
  background: var(--color-bg-glass);
  color: var(--color-secondary);
}

.lang-option:first-child {
  border-radius: 6px 6px 0 0;
}

.lang-option:last-child {
  border-radius: 0 0 6px 6px;
}

/* Responsive Design for Header */
@media (max-width: 768px) {
  .navbar {
    left: 0;
    right: 0;
  }
  
  .nav-container {
    padding: 0 1rem;
  }
  
  .nav-links {
    display: none;
  }
}
</style>
