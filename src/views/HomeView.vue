<template>
  <div id="app">
    <!-- Header Component -->
    <Header />

    <!-- Hero Section -->
    <Hero />

    <!-- About Section -->
    <section id="about" class="about-section">
      <div class="about-background"></div>
      <div class="about-content">
        <div class="about-left scroll-reveal-left">
          <div class="about-card">
            <h2 class="section-title">{{ t('about.title') }}</h2>
            <p class="about-description">{{ t('about.description') }}</p>
            
            <div class="vision-mission">
              <div class="vision hover-lift">
                <h3 class="subsection-title">{{ t('about.vision.title') }}</h3>
                <p class="subsection-description">{{ t('about.vision.description') }}</p>
              </div>
              
              <div class="mission hover-lift">
                <h3 class="subsection-title">{{ t('about.mission.title') }}</h3>
                <p class="subsection-description">{{ t('about.mission.description') }}</p>
              </div>
            </div>
          </div>
        </div>
        
        <div class="about-right scroll-reveal-right">
          <div class="locations-card morphing-shape hover-glow">
            <h3 class="locations-title">{{ t('about.locations.title') }}</h3>
            <p class="locations-subtitle">{{ t('about.locations.subtitle') }}</p>
            
            <div class="location-buttons">
              <div class="location-btn hover-bounce">
                <span class="location-pin animate-float">
                  <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12.5 13.4271C14.2231 13.4271 15.62 12.0302 15.62 10.3071C15.62 8.58398 14.2231 7.1871 12.5 7.1871C10.7769 7.1871 9.38 8.58398 9.38 10.3071C9.38 12.0302 10.7769 13.4271 12.5 13.4271Z" stroke="white" stroke-width="1.5"/>
            <path d="M4.11971 8.4871C6.08971 -0.172897 18.9197 -0.162897 20.8797 8.4971C22.0297 13.5771 18.8697 17.8771 16.0997 20.5371C14.0897 22.4771 10.9097 22.4771 8.88971 20.5371C6.12971 17.8771 2.96971 13.5671 4.11971 8.4871Z" stroke="white" stroke-width="1.5"/>
            </svg>
                </span>
                {{ t('about.locations.riyadh') }}
              </div>
              <div class="location-btn hover-bounce">
                <span class="location-pin animate-float">
                  <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12.5 13.4271C14.2231 13.4271 15.62 12.0302 15.62 10.3071C15.62 8.58398 14.2231 7.1871 12.5 7.1871C10.7769 7.1871 9.38 8.58398 9.38 10.3071C9.38 12.0302 10.7769 13.4271 12.5 13.4271Z" stroke="white" stroke-width="1.5"/>
            <path d="M4.11971 8.4871C6.08971 -0.172897 18.9197 -0.162897 20.8797 8.4971C22.0297 13.5771 18.8697 17.8771 16.0997 20.5371C14.0897 22.4771 10.9097 22.4771 8.88971 20.5371C6.12971 17.8771 2.96971 13.5671 4.11971 8.4871Z" stroke="white" stroke-width="1.5"/>
            </svg>
                </span>
                {{ t('about.locations.abudhabi') }}
              </div>
            </div>
            
            <div class="company-logo">
              <img src="../assets/logo.svg" alt="IltizamTech Logo" class="logo-image">
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Services & Projects Container -->
    <div class="services-projects-container">
      <div class="shared-background"></div>
      
      <!-- Services Section -->
      <section id="services" class="services-section">
      <div class="services-content">
        <h2 class="section-title scroll-reveal">{{ t('services.title') }}</h2>
        
        <div class="services-grid">
          <div class="service-card scroll-reveal-scale hover-lift glass-effect">
            <div class="service-icon animate-float">
              <svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M11.6667 7.49992C10.78 7.49966 9.90921 7.7352 9.14356 8.18238C8.37791 8.62956 7.74495 9.2723 7.30956 10.0447C6.87417 10.8171 6.65201 11.6914 6.66585 12.578C6.67969 13.4645 6.92904 14.3315 7.38834 15.0899C6.24757 15.3103 5.21913 15.921 4.47959 16.8171C3.74005 17.7133 3.33556 18.8389 3.33556 20.0008C3.33556 21.1626 3.74005 22.2882 4.47959 23.1844C5.21913 24.0805 6.24757 24.6912 7.38834 24.9116M11.6667 7.49992C11.6667 6.39485 12.1057 5.33504 12.8871 4.55364C13.6685 3.77224 14.7283 3.33325 15.8333 3.33325C16.9384 3.33325 17.9982 3.77224 18.7796 4.55364C19.561 5.33504 20 6.39485 20 7.49992M11.6667 7.49992C11.6667 8.86325 12.3217 10.0733 13.3333 10.8333M7.38834 24.9116C6.92947 25.67 6.68046 26.5367 6.66684 27.4231C6.65321 28.3094 6.87546 29.1834 7.3108 29.9555C7.74614 30.7277 8.37893 31.3702 9.14434 31.8173C9.90974 32.2644 10.7802 32.5 11.6667 32.4999C11.6667 33.605 12.1057 34.6648 12.8871 35.4462C13.6685 36.2276 14.7283 36.6666 15.8333 36.6666C16.9384 36.6666 17.9982 36.2276 18.7796 35.4462C19.561 34.6648 20 33.605 20 32.4999M7.38834 24.9116C7.98646 23.9214 8.90945 23.1692 10 22.7833M20 7.49992V32.4999M20 7.49992C20 6.39485 20.439 5.33504 21.2204 4.55364C22.0018 3.77224 23.0616 3.33325 24.1667 3.33325C25.2717 3.33325 26.3315 3.77224 27.1129 4.55364C27.8943 5.33504 28.3333 6.39485 28.3333 7.49992C29.2198 7.49984 30.0903 7.73542 30.8557 8.18252C31.6211 8.62961 32.2539 9.27215 32.6892 10.0443C33.1245 10.8164 33.3468 11.6905 33.3332 12.5768C33.3195 13.4631 33.0705 14.3298 32.6117 15.0883M20 32.4999C20 33.605 20.439 34.6648 21.2204 35.4462C22.0018 36.2276 23.0616 36.6666 24.1667 36.6666C25.2717 36.6666 26.3315 36.2276 27.1129 35.4462C27.8943 34.6648 28.3333 33.605 28.3333 32.4999M28.3333 32.4999C29.22 32.5002 30.0908 32.2646 30.8564 31.8175C31.6221 31.3703 32.2551 30.7275 32.6904 29.9551C33.1258 29.1827 33.348 28.3084 33.3342 27.4219C33.3203 26.5353 33.071 25.6684 32.6117 24.9099C33.7524 24.6895 34.7809 24.0788 35.5204 23.1827C36.26 22.2866 36.6645 21.161 36.6645 19.9991C36.6645 18.8372 36.26 17.7116 35.5204 16.8155C34.7809 15.9194 33.7524 15.3087 32.6117 15.0883M28.3333 32.4999C28.3333 31.1366 27.6783 29.9266 26.6667 29.1666M32.6117 15.0883C32.0135 16.0785 31.0906 16.8306 30 17.2166" stroke="white" stroke-width="2.52" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

            </div>
            <h3 class="service-title">{{ t('services.ai.title') }}</h3>
            <p class="service-description">{{ t('services.ai.description') }}</p>
          </div>
          
          <div class="service-card scroll-reveal-scale hover-lift glass-effect">
            <div class="service-icon animate-float">
              <svg width="41" height="42" viewBox="0 0 41 42" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.794 4.56778L9.40172 7.7296C7.46763 8.45278 5.88672 10.7401 5.88672 12.7919V25.2878C5.88672 27.2723 7.19854 29.8791 8.79626 31.0732L16.0281 36.4719C18.3994 38.2546 22.3013 38.2546 24.6726 36.4719L31.9044 31.0732C33.5022 29.8791 34.814 27.2723 34.814 25.2878V12.7919C34.814 10.7232 33.2331 8.43596 31.299 7.71278L22.9067 4.56778C21.4772 4.04642 19.1899 4.04642 17.794 4.56778Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

            </div>
            <h3 class="service-title">{{ t('services.sre.title') }}</h3>
            <p class="service-description">{{ t('services.sre.description') }}</p>
          </div>
          
          <div class="service-card scroll-reveal-scale hover-lift glass-effect">
            <div class="service-icon animate-float"><svg width="41" height="42" viewBox="0 0 41 42" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.0839 22.211H18.0103V29.0224C18.0103 30.0314 19.2548 30.5024 19.9276 29.7455L27.0921 21.6055C27.7144 20.8992 27.2098 19.7892 26.268 19.7892H23.3416V12.9778C23.3416 11.9687 22.0971 11.4978 21.4244 12.2546L14.2598 20.3946C13.6376 21.101 14.1421 22.211 15.0839 22.211Z" stroke="white" stroke-width="2.52273" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M20.6174 37.818C29.9058 37.818 37.4356 30.2882 37.4356 20.9998C37.4356 11.7114 29.9058 4.18164 20.6174 4.18164C11.329 4.18164 3.79919 11.7114 3.79919 20.9998C3.79919 30.2882 11.329 37.818 20.6174 37.818Z" stroke="white" stroke-width="2.52273" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</div>
            <h3 class="service-title">{{ t('services.development.title') }}</h3>
            <p class="service-description">{{ t('services.development.description') }}</p>
          </div>
          
          <div class="service-card scroll-reveal-scale hover-lift glass-effect">
            <div class="service-icon animate-float">
              <svg width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M36.9787 9.81589C36.9787 11.3463 36.2555 12.7086 35.1455 13.5832C34.3382 14.2223 33.3123 14.6091 32.1855 14.6091C29.5282 14.6091 27.3923 12.4732 27.3923 9.81589C27.3923 8.68907 27.7792 7.67998 28.4182 6.85589H28.4351C29.2928 5.74589 30.6551 5.02271 32.1855 5.02271C34.8428 5.02271 36.9787 7.15861 36.9787 9.81589Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M14.6092 9.81589C14.6092 12.4732 12.4733 14.6091 9.81601 14.6091C8.68919 14.6091 7.6801 14.2223 6.85601 13.5832C5.74601 12.7086 5.02283 11.3463 5.02283 9.81589C5.02283 7.15861 7.15874 5.02271 9.81601 5.02271C11.3465 5.02271 12.7087 5.74589 13.5833 6.85589C14.2224 7.67998 14.6092 8.68907 14.6092 9.81589Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M36.9787 32.1838C36.9787 34.8411 34.8428 36.977 32.1855 36.977C30.6551 36.977 29.2928 36.2538 28.4351 35.1438H28.4182C27.7792 34.3365 27.3923 33.3106 27.3923 32.1838C27.3923 29.5265 29.5282 27.3906 32.1855 27.3906C33.3123 27.3906 34.3214 27.7774 35.1455 28.4165V28.4334C36.2555 29.2911 36.9787 30.6534 36.9787 32.1838Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M14.6092 32.1841C14.6092 33.3109 14.2224 34.32 13.5833 35.1441C12.7087 36.2709 11.3465 36.9772 9.81601 36.9772C7.15874 36.9772 5.02283 34.8413 5.02283 32.1841C5.02283 30.6536 5.74601 29.2913 6.85601 28.4336V28.4168C7.66328 27.7777 8.68919 27.3909 9.81601 27.3909C12.4733 27.3909 14.6092 29.5268 14.6092 32.1841Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M36.9774 21C36.9774 23.6909 36.3215 26.1968 35.1442 28.4168C34.3369 27.7777 33.311 27.3909 32.1842 27.3909C29.5269 27.3909 27.391 29.5268 27.391 32.1841C27.391 33.3109 27.7778 34.32 28.4169 35.1441C26.1969 36.3213 23.691 36.9773 21.0001 36.9773C18.326 36.9773 15.8033 36.3213 13.5833 35.1441C14.2224 34.3368 14.6092 33.3109 14.6092 32.1841C14.6092 29.5268 12.4733 27.3909 9.81601 27.3909C8.68919 27.3909 7.6801 27.7777 6.85601 28.4168C5.67874 26.1968 5.02283 23.6909 5.02283 21C5.02283 18.3259 5.67874 15.8032 6.85601 13.5832C7.6801 14.2223 8.68919 14.6091 9.81601 14.6091C12.4733 14.6091 14.6092 12.4732 14.6092 9.81589C14.6092 8.68907 14.2224 7.67998 13.5833 6.85589C15.8033 5.67861 18.326 5.02271 21.0001 5.02271C23.691 5.02271 26.1969 5.67861 28.4169 6.85589C27.7778 7.66316 27.391 8.68907 27.391 9.81589C27.391 12.4732 29.5269 14.6091 32.1842 14.6091C33.311 14.6091 34.3201 14.2223 35.1442 13.5832C36.3215 15.8032 36.9774 18.3259 36.9774 21Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

            </div>
            <h3 class="service-title">{{ t('services.transformation.title') }}</h3>
            <p class="service-description">{{ t('services.transformation.description') }}</p>
          </div>
        </div>
      </div>
      </section>

      <!-- Projects Section -->
      <section id="projects" class="projects-section">
      <div class="projects-content">
        <h2 class="section-title scroll-reveal">{{ t('projects.title') }}</h2>
        <p class="section-subtitle scroll-reveal">{{ t('projects.subtitle') }}</p>
        
        <div class="project-card scroll-reveal-scale hover-lift glass-effect">
          <div class="project-header">
            <div class="project-logo">
              <img src="../assets/logo.svg" alt="IltizamTech Logo" class="project-logo-image">
              <div class="logo-content">
                <span class="logo-text">{{ t('nav.companyName') }}</span>
                <p class="project-tagline">{{ t('nav.tagline') }}</p>
              </div>
            </div>
          </div>
          
          <h3 class="project-title">{{ t('projects.inspectz.title') }}</h3>
          <p class="project-description">{{ t('projects.inspectz.description') }}</p>
          
          <div class="project-details">
            <div class="features-column scroll-reveal-left hover-lift">
              <h4 class="details-title">{{ t('projects.inspectz.features.title') }}</h4>
              <ul class="features-list">
                <li class="hover-bounce">
                  <span class="checkmark animate-pulse"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.5002C22.375 27.5002 28 21.8752 28 15.0002C28 8.12524 22.375 2.50024 15.5 2.50024C8.625 2.50024 3 8.12524 3 15.0002C3 21.8752 8.625 27.5002 15.5 27.5002Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.features.dashboard') }}
                </li>
                <li class="hover-bounce">
                  <span class="checkmark animate-pulse"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.5002C22.375 27.5002 28 21.8752 28 15.0002C28 8.12524 22.375 2.50024 15.5 2.50024C8.625 2.50024 3 8.12524 3 15.0002C3 21.8752 8.625 27.5002 15.5 27.5002Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.features.detection') }}
                </li>
                <li class="hover-bounce">
                  <span class="checkmark animate-pulse"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.5002C22.375 27.5002 28 21.8752 28 15.0002C28 8.12524 22.375 2.50024 15.5 2.50024C8.625 2.50024 3 8.12524 3 15.0002C3 21.8752 8.625 27.5002 15.5 27.5002Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.features.mobile') }}
                </li>
              </ul>
            </div>
            
            <div class="technologies-column">
              <h4 class="details-title">{{ t('projects.inspectz.technologies.title') }}</h4>
              <ul class="technologies-list">
                <li>
                  <span class="checkmark"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.125 11.875L15.875 17.125L13.875 14.125L9.875 18.125" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.625 11.875H21.125V14.375" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M11.7501 27.5002H19.2501C25.5001 27.5002 28.0001 25.0002 28.0001 18.7502V11.2502C28.0001 5.00024 25.5001 2.50024 19.2501 2.50024H11.7501C5.50006 2.50024 3.00006 5.00024 3.00006 11.2502V18.7502C3.00006 25.0002 5.50006 27.5002 11.7501 27.5002Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.technologies.netcore') }}
                </li>
                <li>
                  <span class="checkmark"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.125 11.875L15.875 17.125L13.875 14.125L9.875 18.125" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.625 11.875H21.125V14.375" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M11.7501 27.5002H19.2501C25.5001 27.5002 28.0001 25.0002 28.0001 18.7502V11.2502C28.0001 5.00024 25.5001 2.50024 19.2501 2.50024H11.7501C5.50006 2.50024 3.00006 5.00024 3.00006 11.2502V18.7502C3.00006 25.0002 5.50006 27.5002 11.7501 27.5002Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.technologies.flutter') }}
                </li>
                <li>
                  <span class="checkmark"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.125 11.875L15.875 17.125L13.875 14.125L9.875 18.125" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.625 11.875H21.125V14.375" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M11.7501 27.5002H19.2501C25.5001 27.5002 28.0001 25.0002 28.0001 18.7502V11.2502C28.0001 5.00024 25.5001 2.50024 19.2501 2.50024H11.7501C5.50006 2.50024 3.00006 5.00024 3.00006 11.2502V18.7502C3.00006 25.0002 5.50006 27.5002 11.7501 27.5002Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.technologies.arcgi') }}
                </li>
                <li>
                  <span class="checkmark"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.125 11.875L15.875 17.125L13.875 14.125L9.875 18.125" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.625 11.875H21.125V14.375" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M11.7501 27.5002H19.2501C25.5001 27.5002 28.0001 25.0002 28.0001 18.7502V11.2502C28.0001 5.00024 25.5001 2.50024 19.2501 2.50024H11.7501C5.50006 2.50024 3.00006 5.00024 3.00006 11.2502V18.7502C3.00006 25.0002 5.50006 27.5002 11.7501 27.5002Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.technologies.angular') }}
                </li>
                <li>
                  <span class="checkmark"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.125 11.875L15.875 17.125L13.875 14.125L9.875 18.125" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.625 11.875H21.125V14.375" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M11.7501 27.5002H19.2501C25.5001 27.5002 28.0001 25.0002 28.0001 18.7502V11.2502C28.0001 5.00024 25.5001 2.50024 19.2501 2.50024H11.7501C5.50006 2.50024 3.00006 5.00024 3.00006 11.2502V18.7502C3.00006 25.0002 5.50006 27.5002 11.7501 27.5002Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.technologies.nlp') }}
                </li>
                <li>
                  <span class="checkmark"><svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.125 11.875L15.875 17.125L13.875 14.125L9.875 18.125" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M18.625 11.875H21.125V14.375" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M11.7501 27.5002H19.2501C25.5001 27.5002 28.0001 25.0002 28.0001 18.7502V11.2502C28.0001 5.00024 25.5001 2.50024 19.2501 2.50024H11.7501C5.50006 2.50024 3.00006 5.00024 3.00006 11.2502V18.7502C3.00006 25.0002 5.50006 27.5002 11.7501 27.5002Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
</span>
                  {{ t('projects.inspectz.technologies.ml') }}
                </li>
              </ul>
            </div>
          </div>
          
          <button class="project-cta btn-magnetic hover-lift scroll-reveal">
            {{ t('projects.inspectz.cta') }}
            <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M4.16669 10H15.8334M15.8334 10L10.8334 5M15.8334 10L10.8334 15" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </button>
        </div>
      </div>
      </section>
      
      <!-- Project Info Cards -->
      <div class="project-info-grid scroll-reveal">
        <div class="project-info-card scroll-reveal-left hover-lift glass-effect">
          <h3 class="info-card-title">{{ t('contact.whoWeServe.title') }}</h3>
          <ul class="info-list">
            <li class="hover-bounce">
              <span class="checkmark animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.4995C22.375 27.4995 28 21.8745 28 14.9995C28 8.12451 22.375 2.49951 15.5 2.49951C8.62498 2.49951 2.99998 8.12451 2.99998 14.9995C2.99998 21.8745 8.62498 27.4995 15.5 27.4995Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whoWeServe.government') }}
            </li>
            <li class="hover-bounce">
              <span class="checkmark animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.4995C22.375 27.4995 28 21.8745 28 14.9995C28 8.12451 22.375 2.49951 15.5 2.49951C8.62498 2.49951 2.99998 8.12451 2.99998 14.9995C2.99998 21.8745 8.62498 27.4995 15.5 27.4995Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whoWeServe.public') }}
            </li>
            <li class="hover-bounce">
              <span class="checkmark animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.4995C22.375 27.4995 28 21.8745 28 14.9995C28 8.12451 22.375 2.49951 15.5 2.49951C8.62498 2.49951 2.99998 8.12451 2.99998 14.9995C2.99998 21.8745 8.62498 27.4995 15.5 27.4995Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whoWeServe.enterprises') }}
            </li>
            <li class="hover-bounce">
              <span class="checkmark animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 27.4995C22.375 27.4995 28 21.8745 28 14.9995C28 8.12451 22.375 2.49951 15.5 2.49951C8.62498 2.49951 2.99998 8.12451 2.99998 14.9995C2.99998 21.8745 8.62498 27.4995 15.5 27.4995Z" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M10.1875 14.9999L13.725 18.5374L20.8125 11.4624" stroke="#1FC16B" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whoWeServe.partners') }}
            </li>
          </ul>
        </div>
        
        <div class="project-info-card scroll-reveal-right hover-lift glass-effect">
          <h3 class="info-card-title">{{ t('contact.whyChoose.title') }}</h3>
          <ul class="info-list">
            <li class="hover-bounce">
              <span class="star animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.6623 4.3873L19.8623 8.78731C20.1623 9.39981 20.9623 9.9873 21.6373 10.0998L25.6248 10.7623C28.1748 11.1873 28.7748 13.0373 26.9373 14.8623L23.8373 17.9623C23.3123 18.4873 23.0248 19.4998 23.1873 20.2248L24.0748 24.0623C24.7748 27.0998 23.1623 28.2748 20.4748 26.6873L16.7373 24.4748C16.0623 24.0748 14.9498 24.0748 14.2623 24.4748L10.5248 26.6873C7.84983 28.2748 6.22483 27.0873 6.92483 24.0623L7.81233 20.2248C7.97483 19.4998 7.68733 18.4873 7.16233 17.9623L4.06233 14.8623C2.23733 13.0373 2.82483 11.1873 5.37483 10.7623L9.36233 10.0998C10.0248 9.9873 10.8248 9.39981 11.1248 8.78731L13.3248 4.3873C14.5248 1.9998 16.4748 1.9998 17.6623 4.3873Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whyChoose.expertise') }}
            </li>
            <li class="hover-bounce">
              <span class="star animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.6623 4.3873L19.8623 8.78731C20.1623 9.39981 20.9623 9.9873 21.6373 10.0998L25.6248 10.7623C28.1748 11.1873 28.7748 13.0373 26.9373 14.8623L23.8373 17.9623C23.3123 18.4873 23.0248 19.4998 23.1873 20.2248L24.0748 24.0623C24.7748 27.0998 23.1623 28.2748 20.4748 26.6873L16.7373 24.4748C16.0623 24.0748 14.9498 24.0748 14.2623 24.4748L10.5248 26.6873C7.84983 28.2748 6.22483 27.0873 6.92483 24.0623L7.81233 20.2248C7.97483 19.4998 7.68733 18.4873 7.16233 17.9623L4.06233 14.8623C2.23733 13.0373 2.82483 11.1873 5.37483 10.7623L9.36233 10.0998C10.0248 9.9873 10.8248 9.39981 11.1248 8.78731L13.3248 4.3873C14.5248 1.9998 16.4748 1.9998 17.6623 4.3873Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whyChoose.trackRecord') }}
            </li>
            <li class="hover-bounce">
              <span class="star animate-pulse">
              <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.6623 4.3873L19.8623 8.78731C20.1623 9.39981 20.9623 9.9873 21.6373 10.0998L25.6248 10.7623C28.1748 11.1873 28.7748 13.0373 26.9373 14.8623L23.8373 17.9623C23.3123 18.4873 23.0248 19.4998 23.1873 20.2248L24.0748 24.0623C24.7748 27.0998 23.1623 28.2748 20.4748 26.6873L16.7373 24.4748C16.0623 24.0748 14.9498 24.0748 14.2623 24.4748L10.5248 26.6873C7.84983 28.2748 6.22483 27.0873 6.92483 24.0623L7.81233 20.2248C7.97483 19.4998 7.68733 18.4873 7.16233 17.9623L4.06233 14.8623C2.23733 13.0373 2.82483 11.1873 5.37483 10.7623L9.36233 10.0998C10.0248 9.9873 10.8248 9.39981 11.1248 8.78731L13.3248 4.3873C14.5248 1.9998 16.4748 1.9998 17.6623 4.3873Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whyChoose.bilingual') }}
            </li>
            <li class="hover-bounce">
              <span class="star animate-pulse">
                <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.6623 4.3873L19.8623 8.78731C20.1623 9.39981 20.9623 9.9873 21.6373 10.0998L25.6248 10.7623C28.1748 11.1873 28.7748 13.0373 26.9373 14.8623L23.8373 17.9623C23.3123 18.4873 23.0248 19.4998 23.1873 20.2248L24.0748 24.0623C24.7748 27.0998 23.1623 28.2748 20.4748 26.6873L16.7373 24.4748C16.0623 24.0748 14.9498 24.0748 14.2623 24.4748L10.5248 26.6873C7.84983 28.2748 6.22483 27.0873 6.92483 24.0623L7.81233 20.2248C7.97483 19.4998 7.68733 18.4873 7.16233 17.9623L4.06233 14.8623C2.23733 13.0373 2.82483 11.1873 5.37483 10.7623L9.36233 10.0998C10.0248 9.9873 10.8248 9.39981 11.1248 8.78731L13.3248 4.3873C14.5248 1.9998 16.4748 1.9998 17.6623 4.3873Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whyChoose.comprehensive') }}
            </li>
            <li class="hover-bounce">
              <span class="star animate-pulse">
                <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M17.6623 4.3873L19.8623 8.78731C20.1623 9.39981 20.9623 9.9873 21.6373 10.0998L25.6248 10.7623C28.1748 11.1873 28.7748 13.0373 26.9373 14.8623L23.8373 17.9623C23.3123 18.4873 23.0248 19.4998 23.1873 20.2248L24.0748 24.0623C24.7748 27.0998 23.1623 28.2748 20.4748 26.6873L16.7373 24.4748C16.0623 24.0748 14.9498 24.0748 14.2623 24.4748L10.5248 26.6873C7.84983 28.2748 6.22483 27.0873 6.92483 24.0623L7.81233 20.2248C7.97483 19.4998 7.68733 18.4873 7.16233 17.9623L4.06233 14.8623C2.23733 13.0373 2.82483 11.1873 5.37483 10.7623L9.36233 10.0998C10.0248 9.9873 10.8248 9.39981 11.1248 8.78731L13.3248 4.3873C14.5248 1.9998 16.4748 1.9998 17.6623 4.3873Z" stroke="white" stroke-width="2.52273" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

              </span>
              {{ t('contact.whyChoose.commitment') }}
            </li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Contact Section -->
    <section id="contact" class="contact-section">
      <div class="contact-background"></div>
      <div class="contact-content">
        
        <h2 class="contact-main-title scroll-reveal">{{ t('contact.title') }}</h2>
        
        <div class="contact-info-grid">
          <div class="contact-card locations scroll-reveal-left hover-lift glass-effect">
            <h3 class="card-title">{{ t('contact.locations.title') }}</h3>
            <ul class="locations-list">
              <li class="hover-bounce">
                <span class="location-pin animate-float">
                  <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 16.7873C17.6539 16.7873 19.4 15.0412 19.4 12.8873C19.4 10.7334 17.6539 8.9873 15.5 8.9873C13.3461 8.9873 11.6 10.7334 11.6 12.8873C11.6 15.0412 13.3461 16.7873 15.5 16.7873Z" stroke="#1FC16B" stroke-width="2"/>
<path d="M5.02461 10.612C7.48711 -0.212986 23.5246 -0.200485 25.9746 10.6245C27.4121 16.9745 23.4621 22.3495 19.9996 25.6745C17.4871 28.0995 13.5121 28.0995 10.9871 25.6745C7.53711 22.3495 3.58711 16.962 5.02461 10.612Z" stroke="#1FC16B" stroke-width="2"/>
</svg>

                </span>
                {{ t('contact.locations.riyadh') }}
              </li>
              <li class="hover-bounce">
                <span class="location-pin animate-float">
                  <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M15.5 16.7873C17.6539 16.7873 19.4 15.0412 19.4 12.8873C19.4 10.7334 17.6539 8.9873 15.5 8.9873C13.3461 8.9873 11.6 10.7334 11.6 12.8873C11.6 15.0412 13.3461 16.7873 15.5 16.7873Z" stroke="#1FC16B" stroke-width="2"/>
<path d="M5.02461 10.612C7.48711 -0.212986 23.5246 -0.200485 25.9746 10.6245C27.4121 16.9745 23.4621 22.3495 19.9996 25.6745C17.4871 28.0995 13.5121 28.0995 10.9871 25.6745C7.53711 22.3495 3.58711 16.962 5.02461 10.612Z" stroke="#1FC16B" stroke-width="2"/>
</svg>

                </span>
                {{ t('contact.locations.abudhabi') }}
              </li>
            </ul>
          </div>
          
          <div class="contact-card contact-info scroll-reveal-right hover-lift glass-effect">
            <h3 class="card-title">{{ t('contact.info.title') }}</h3>
            <ul class="info-list">
              <li class="hover-bounce">
                <span class="email-icon animate-float">
                  <svg width="31" height="30" viewBox="0 0 31 30" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.7501 25.6255H9.25006C5.50006 25.6255 3.00006 23.7505 3.00006 19.3755V10.6255C3.00006 6.25049 5.50006 4.37549 9.25006 4.37549H21.7501C25.5001 4.37549 28.0001 6.25049 28.0001 10.6255V19.3755C28.0001 23.7505 25.5001 25.6255 21.7501 25.6255Z" stroke="white" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M21.75 11.2495L17.8375 14.3745C16.55 15.3995 14.4375 15.3995 13.15 14.3745L9.25 11.2495" stroke="white" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

                </span>
                {{ t('contact.info.email') }}
              </li>
              <li class="hover-bounce">
                <span class="website-icon animate-float">
                  <svg width="30" height="30" viewBox="0 0 26 27" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M2.65953 9.44984H23.3414M2.65953 16.8362H23.3414M1.9209 13.143C1.9209 14.598 2.20748 16.0387 2.76428 17.383C3.32108 18.7272 4.13719 19.9486 5.16602 20.9774C6.19485 22.0063 7.41625 22.8224 8.76049 23.3792C10.1047 23.936 11.5455 24.2226 13.0004 24.2226C14.4554 24.2226 15.8962 23.936 17.2404 23.3792C18.5846 22.8224 19.806 22.0063 20.8349 20.9774C21.8637 19.9486 22.6798 18.7272 23.2366 17.383C23.7934 16.0387 24.08 14.598 24.08 13.143C24.08 10.2045 22.9127 7.38642 20.8349 5.3086C18.757 3.23078 15.9389 2.06348 13.0004 2.06348C10.062 2.06348 7.24384 3.23078 5.16602 5.3086C3.0882 7.38642 1.9209 10.2045 1.9209 13.143Z" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M12.3853 2.06348C10.3114 5.38686 9.21191 9.22562 9.21191 13.143C9.21191 17.0604 10.3114 20.8992 12.3853 24.2226M13.6164 2.06348C15.6903 5.38686 16.7898 9.22562 16.7898 13.143C16.7898 17.0604 15.6903 20.8992 13.6164 24.2226" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
                </span>
                {{ t('contact.info.website') }}
              </li>
            </ul>
          </div>
        </div>
        
        <button class="contact-cta btn-magnetic hover-lift scroll-reveal" @click="scrollToHero">
          {{ t('contact.cta') }} 
          <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M14.9297 5.92725L20.9997 11.9972L14.9297 18.0672" stroke="white" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M4 11.9971H20.83" stroke="white" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>
    </section>
    
    <!-- Footer Section -->
    <Footer />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { useI18n } from 'vue-i18n'
import Header from '@/components/Header.vue'
import Hero from '@/components/Hero.vue'
import Footer from '@/components/Footer.vue'

const { locale, t } = useI18n()
const currentLocale = ref('en')

const scrollToHero = () => {
  const element = document.getElementById('hero')
  if (element) {
    element.scrollIntoView({ 
      behavior: 'smooth',
      block: 'start',
      inline: 'nearest'
    })
  }
}


onMounted(() => {
  // Load saved language from localStorage, fallback to English
  const savedLang = localStorage.getItem('iltizamtech-language')
  if (savedLang && (savedLang === 'en' || savedLang === 'ar')) {
    currentLocale.value = savedLang
    locale.value = savedLang
    document.documentElement.dir = savedLang === 'ar' ? 'rtl' : 'ltr'
    document.documentElement.lang = savedLang
  } else {
    document.documentElement.dir = 'ltr'
    document.documentElement.lang = 'en'
  }

  // Initialize scroll animations
  initScrollAnimations()
})

const initScrollAnimations = () => {
  const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
  }

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('revealed')
      }
    })
  }, observerOptions)

  // Observe all scroll-reveal elements
  const scrollElements = document.querySelectorAll('.scroll-reveal, .scroll-reveal-left, .scroll-reveal-right, .scroll-reveal-scale')
  scrollElements.forEach(el => observer.observe(el))
}
</script>