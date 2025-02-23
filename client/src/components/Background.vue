<template>
    <div class="relative w-full min-h-screen overflow-hidden">
      <!-- Fading dot grid -->
      <div class="dot-grid absolute inset-0"></div>
     
      <!-- Meteor shower -->
      <div class="absolute inset-0">
        <div class="meteor-1 meteor"></div>
        <div class="meteor-2 meteor"></div>
        <div class="meteor-3 meteor"></div>
        <div class="meteor-4 meteor"></div>
        <div class="meteor-5 meteor"></div>
        <div class="meteor-6 meteor"></div>
        <div class="meteor-7 meteor"></div>
        <div class="meteor-8 meteor"></div>
      </div>
      <!-- Slot for wrapped content -->
      <div class="relative z-10">
        <slot></slot>
      </div>
    </div>
  </template>
  
  <script setup>
  // No script needed
  </script>
  
  <style scoped>
  .dot-grid {
    background-image: radial-gradient(rgb(0, 0, 0) 1.5px, transparent 1.5px);
    background-size: 50px 50px;
    pointer-events: none;
    mask-image: radial-gradient(
      circle at center,
      transparent 30%,
      rgba(0, 0, 0, 0.2) 45%,
      rgba(0, 0, 0, 0.5) 80%,
      rgba(0, 0, 0, 0.7) 100%
    );
    -webkit-mask-image: radial-gradient(
      circle at center,
      transparent 30%,
      rgba(0, 0, 0, 0.2) 45%,
      rgba(0, 0, 0, 0.5) 80%,
      rgba(0, 0, 0, 0.7) 100%
    );
  }
  
  .meteor {
    position: absolute;
    width: 4px;
    height: 4px;
    background: #333;
    border-radius: 50%;
    animation: meteor 4s linear infinite;
    opacity: 0;
  }
  
  .meteor::before {
    content: '';
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 100px;
    height: 2px;
    background: linear-gradient(-90deg, #333, transparent);
    opacity: 0.4;
    right: 0;
  }
  
  /* Repositioned meteors to concentrate near the top */
  .meteor-1 { top: 5%; left: 5%; animation-delay: 0s; }
  .meteor-2 { top: 8%; left: 15%; animation-delay: 0.4s; }
  .meteor-3 { top: 12%; left: 25%; animation-delay: 0.8s; }
  .meteor-4 { top: 15%; left: 10%; animation-delay: 1.2s; }
  .meteor-5 { top: 18%; left: 20%; animation-delay: 1.6s; }
  .meteor-6 { top: 22%; left: 8%; animation-delay: 2.0s; }
  .meteor-7 { top: 25%; left: 18%; animation-delay: 2.4s; }
  .meteor-8 { top: 28%; left: 12%; animation-delay: 2.8s; }
  
  @keyframes meteor {
    0% {
      opacity: 1;
      transform: translate(0, 0) rotate(45deg);
    }
   
    95% {
      opacity: 1;
    }
    100% {
      opacity: 0;
      transform: translate(1000px, 1000px) rotate(45deg);
    }
  }
  </style>