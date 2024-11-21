<script setup lang="ts">
import { RouterLink } from 'vue-router';
</script>

<template>
  <section class="fixed top-0 left-0 w-full bg-white opacity-0 transition-opacity duration-500 hover:opacity-100 shadow-md z-50 h-18">
  <div class="navbar">
    <div class="navbar-start">
      <div class="dropdown">
        <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" />
          </svg>
        </div>
        <ul tabindex="0" class="menu menu-sm dropdown-content bg-base-100 rounded-box z-[1] mt-3 w-24 p-2 shadow">
          <RouterLink to="/">
            <li><a href="#header">Home</a></li>
          </RouterLink>
          <li><a href="#experience">Experience</a></li>
        </ul>
      </div>
      <!-- <RouterLink to="/"><a class="btn btn-ghost text-xl">Yoosup Song</a></RouterLink> -->
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
          <li><a href="#header" class="text-xl text-bold">Home</a></li>
        <li><a href="#experience" class="text-xl text-bold">Experience</a></li>
      </ul>
    </div>
    <div class="navbar-end">
    </div>
  </div>
</section>
</template>

<style scoped>
</style>