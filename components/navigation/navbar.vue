<script setup>
import { ref } from 'vue';

const isOpen = ref(false);
</script>
<template>
  <nav class="bg-white shadow-md">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between items-center">
        <div class="flex space-x-4">
          <!-- logo -->
          <div>
            <a href="#" class="flex items-center py-5 px-2 text-gray-700 hover:text-gray-900">
              <!-- Logo and company name -->
              <span class="font-bold">Brand</span>
            </a>
          </div>
          <!-- primary nav -->
          <div class="hidden md:flex items-center space-x-1">
            <a href="#" class="py-5 px-3 text-gray-700 hover:text-gray-900">Home</a>
            <a href="#" class="py-5 px-3 text-gray-700 hover:text-gray-900">Careers</a>
            <a href="#" class="py-5 px-3 text-gray-700 hover:text-gray-900">Blog</a>
            <a href="#" class="py-5 px-3 text-gray-700 hover:text-gray-900">Contact Us</a>
          </div>
        </div>
        <!-- search bar -->
        <div class="flex items-center">
          <input type="search" class="hidden md:block w-full md:max-w-xs rounded-md border-2 focus:outline-none border-gray-300 px-4 py-2 mr-4" placeholder="Search" />
        </div>
        <!-- mobile button -->
        <div class="md:hidden flex items-center">
          <button @click="isOpen = !isOpen" class="md:hidden">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
          </button>
        </div>
      </div>
    </div>
    <!-- mobile menu -->
    <div class="md:hidden" :class="isOpen ? 'block' : 'hidden'">
      <a href="#" class="block py-2 px-4 text-sm hover:bg-gray-200">Home</a>
      <a href="#" class="block py-2 px-4 text-sm hover:bg-gray-200">Careers</a>
      <a href="#" class="block py-2 px-4 text-sm hover:bg-gray-200">Blog</a>
      <a href="#" class="block py-2 px-4 text-sm hover:bg-gray-200">Contact Us</a>
      <!-- mobile search bar -->
      <input type="search" class="w-full rounded-md border-gray-300 px-4 py-2 my-2" placeholder="Search" />
    </div>
  </nav>
</template>