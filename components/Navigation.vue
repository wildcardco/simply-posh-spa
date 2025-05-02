<template>
  <nav class="bg-white shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-20">
        <div class="flex items-center">
          <NuxtLink to="/" class="flex-shrink-0 flex items-center">
            <h1 class="text-2xl font-display font-bold text-gray-900">Simply Posh Salon and Spa</h1>
          </NuxtLink>
        </div>
        
        <!-- Desktop Navigation -->
        <div class="hidden sm:flex sm:space-x-8 sm:items-center">
          <NuxtLink 
            v-for="item in navigationItems" 
            :key="item.path"
            :to="item.path"
            class="text-gray-700 hover:text-spa-gold px-3 py-2 text-sm font-medium transition-colors"
          >
            {{ item.name }}
          </NuxtLink>
        </div>

        <!-- Mobile Navigation Button -->
        <div class="flex items-center sm:hidden">
          <button 
            @click="mobileMenuOpen = !mobileMenuOpen"
            class="inline-flex items-center justify-center p-2 rounded-md text-gray-700 hover:text-gray-900 hover:bg-gray-100"
          >
            <span class="sr-only">Open main menu</span>
            <svg 
              class="h-6 w-6" 
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path 
                v-if="!mobileMenuOpen" 
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M4 6h16M4 12h16M4 18h16"
              />
              <path 
                v-else 
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Navigation Menu -->
    <TransitionRoot as="template" :show="mobileMenuOpen">
      <div class="sm:hidden">
        <div class="pt-2 pb-3 space-y-1">
          <NuxtLink
            v-for="item in navigationItems"
            :key="item.path"
            :to="item.path"
            class="block px-3 py-2 text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
            @click="mobileMenuOpen = false"
          >
            {{ item.name }}
          </NuxtLink>
        </div>
      </div>
    </TransitionRoot>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { TransitionRoot } from '@headlessui/vue'

const mobileMenuOpen = ref(false)

const navigationItems = [
  { name: 'Home', path: '/' },
  { name: 'Before & After', path: '/gallery' },
  { name: 'Services', path: '/services' },
  { name: 'Reviews', path: '/reviews' }
]
</script>