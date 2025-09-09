<script setup lang="ts">
import { onMounted } from "vue";
import HeaderComponent from './components/HeaderComponent.vue';
import HeroComponent from "./components/HeroComponent.vue";

// Declaração para o TypeScript reconhecer particlesJS 
onMounted(() => {
  console.log('App mounted');
  const container = document.getElementById('particles-js');
  if (!container) {
    console.error('particles-js container not found');
    return;
  }
  if (!window.particlesJS) {
    const script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js';
    script.onload = () => {
      console.log('particles.js script loaded');
      if (window.particlesJS) {
            window.particlesJS('particles-js', {
              particles: {
                number: { value: 50 },
                color: { value: "#4169E1" },
                shape: { type: "triangle" },
                opacity: { value: 0.5 },
                size: { value: 3 },
                move: { enable: true, speed: 2 },
                line_linked: {
                  enable: true,
                  distance: 150,
                  color: "#4169E1",
                  opacity: 0.4,
                  width: 1
                }
              },
              interactivity: {
                events: {
                  onhover: { enable: true, mode: "repulse" },
                },
              },
              background: {
                color: "#ffffff"
              }
            });
      } else {
        console.error('particlesJS not found after script load');
      }
    };
    document.body.appendChild(script);
  } else {
    console.log('particlesJS already loaded');
    window.particlesJS('particles-js', {
      particles: {
        number: { value: 50 },
        color: { value: "#4169E1" },
        shape: { type: "circle" },
        opacity: { value: 0.5 },
        size: { value: 3 },
        move: { enable: true, speed: 2 },
      },
      interactivity: {
        events: {
          onhover: { enable: true, mode: "repulse" },
        },
      },
      background: {
        color: "#ffffff"
      }
    });
  }
});


</script>





<template>
  <div id="particles-js" style="position: fixed; top: 0; left: 0; width: 100vw; height: 100vh; z-index: 0; pointer-events: none;"></div>
  <div class="app">
    <!-- Conteúdo da sua app -->
    <div class="app-content">
      <HeaderComponent></HeaderComponent>
      <HeroComponent></HeroComponent>
    </div>
  </div>
</template>





<style>
.app {
  position: relative;
  width: 100%;
  min-height: 100vh;
  z-index: 1;
  background: transparent;
}



.app-content {
  position: relative;
  z-index: 1;
  color: #000;
  background: transparent;
}
</style>
