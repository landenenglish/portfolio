<script setup lang="ts">
const githubUsername = 'landenenglish'
const linkedInUrl = 'https://www.linkedin.com/in/landenenglish' // Update if different
</script>

<template>
  <main class="container">
    <div class="hero">
      <div class="greeting">
        <span class="wave">👋</span>
        <span class="intro">Hey, I'm</span>
      </div>
      
      <h1 class="name">Landen English</h1>
      
      <p class="tagline">
        Software Engineer
      </p>
      
      <div class="links">
        <a 
          :href="`https://github.com/${githubUsername}`" 
          target="_blank" 
          rel="noopener noreferrer"
          class="link-card"
        >
          <svg class="icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
          </svg>
          <span class="link-text">GitHub</span>
          <svg class="arrow" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M7 17L17 7M17 7H7M17 7V17"/>
          </svg>
        </a>

        <a 
          :href="linkedInUrl" 
          target="_blank" 
          rel="noopener noreferrer"
          class="link-card"
        >
          <svg class="icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
          </svg>
          <span class="link-text">LinkedIn</span>
          <svg class="arrow" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M7 17L17 7M17 7H7M17 7V17"/>
          </svg>
        </a>
        
        <a 
          href="/Landen_English_Resume.pdf" 
          target="_blank"
          class="link-card"
        >
          <svg class="icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8l-6-6zm-1 2l5 5h-5V4zM6 20V4h6v6h6v10H6z"/>
            <path d="M8 12h8v2H8zM8 16h8v2H8z"/>
          </svg>
          <span class="link-text">Resume</span>
          <svg class="arrow" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M7 17L17 7M17 7H7M17 7V17"/>
          </svg>
        </a>
      </div>
    </div>
    
    <div class="ambient-orb"></div>
  </main>
</template>

<style scoped>
.container {
  position: relative;
  width: 100%;
  max-width: 600px;
  text-align: center;
}

.hero {
  position: relative;
  z-index: 1;
}

.greeting {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  margin-bottom: 1rem;
  opacity: 0;
  animation: fadeInUp 0.6s ease forwards;
}

.wave {
  font-size: 2rem;
  display: inline-block;
  animation: wave 2.5s ease-in-out infinite;
  transform-origin: 70% 70%;
}

.intro {
  font-size: 1.25rem;
  color: var(--text-secondary);
  font-weight: 400;
}

.name {
  font-size: clamp(2.5rem, 8vw, 4.5rem);
  font-weight: 700;
  letter-spacing: -0.03em;
  line-height: 1.1;
  background: linear-gradient(135deg, var(--text-primary) 0%, var(--text-secondary) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  opacity: 0;
  animation: fadeInUp 0.6s ease 0.1s forwards;
}

.tagline {
  font-size: 1.25rem;
  color: var(--text-secondary);
  margin-top: 1rem;
  font-weight: 400;
  opacity: 0;
  animation: fadeInUp 0.6s ease 0.2s forwards;
}

.links {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-top: 2.5rem;
  flex-wrap: wrap;
  opacity: 0;
  animation: fadeInUp 0.6s ease 0.3s forwards;
}

.link-card {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 1rem 1.5rem;
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 12px;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
}

.link-card:hover {
  background: rgba(255, 255, 255, 0.06);
  border-color: rgba(255, 255, 255, 0.15);
  transform: translateY(-2px);
}

.link-card:hover .arrow {
  transform: translate(2px, -2px);
}

.icon {
  width: 20px;
  height: 20px;
  color: var(--accent);
}

.link-text {
  font-size: 1rem;
  font-weight: 500;
}

.arrow {
  width: 16px;
  height: 16px;
  color: var(--text-secondary);
  transition: transform 0.3s ease;
}

.ambient-orb {
  position: absolute;
  width: 400px;
  height: 400px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  pointer-events: none;
  z-index: 0;
  animation: pulse 8s ease-in-out infinite;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes wave {
  0%, 100% { transform: rotate(0deg); }
  10% { transform: rotate(14deg); }
  20% { transform: rotate(-8deg); }
  30% { transform: rotate(14deg); }
  40% { transform: rotate(-4deg); }
  50% { transform: rotate(10deg); }
  60%, 100% { transform: rotate(0deg); }
}

@keyframes pulse {
  0%, 100% {
    transform: translate(-50%, -50%) scale(1);
    opacity: 0.5;
  }
  50% {
    transform: translate(-50%, -50%) scale(1.1);
    opacity: 0.3;
  }
}

@media (max-width: 480px) {
  .links {
    flex-direction: column;
    align-items: center;
  }
  
  .link-card {
    width: 100%;
    max-width: 200px;
    justify-content: center;
  }
}
</style>
