<template>
  <!-- Footer Section -->
  <footer class="footer-section">
    <div class="footer-content">
      <div class="footer-logo scroll-reveal-scale">
        <img src="../assets/logo.svg" alt="IltizamTech Logo" class="footer-logo-img">
        <div class="logo-text-container">
          <span class="logo-text">{{ t('footer.companyName') }}</span>
          <p class="footer-tagline">{{ t('footer.tagline') }}</p>
        </div>
      </div>
      <p class="footer-description scroll-reveal">{{ t('footer.description') }}</p>
      <p class="footer-copyright scroll-reveal">{{ t('footer.copyright') }}</p>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<style scoped>
.footer-section {
  background: var(--color-bg-primary);
  background-image: url('../assets/images/ltzam-pattern.svg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: var(--spacing-2xl) var(--spacing-lg);
  position: relative;
  display: flex;
  align-items: center;
}

.footer-content {
  text-align: center;
  color: var(--color-text-primary);
  max-width: 800px;
  margin: 0 auto;
  width: 100%;
}

.footer-logo {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  gap: 20px;
  margin-bottom: var(--spacing-md);
}

.footer-logo-img {
  width: 80px;
  height: 80px;
}

.logo-text-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: var(--spacing-xs);
}

.footer-tagline {
  font-size: var(--text-sm);
  color: var(--color-text-secondary);
  margin: 0;
  font-weight: var(--font-medium);
}

.footer-description {
  font-size: var(--text-sm);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-lg);
  line-height: 1.6;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.footer-copyright {
  font-size: var(--text-xs);
  color: var(--color-text-muted);
}
</style>
