<template>
  <main class="py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h1 class="text-4xl font-display font-bold text-center text-gray-900 mb-12">Our Services</h1>

      <!-- Basic Services -->
      <div class="mb-16">
        <h2 class="text-2xl font-display font-semibold text-gray-900 mb-8">Basic Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="service in basicServices" :key="service.type" 
               class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
            <div class="flex items-center justify-center w-12 h-12 bg-spa-pink rounded-full mb-4">
              <svg class="w-6 h-6 text-spa-gold" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                      d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
              </svg>
            </div>
            <h3 class="text-xl font-display font-semibold text-gray-900 mb-2">{{ service.type }}</h3>
            <p class="text-gray-600 mb-4">Includes wash, dry, cut, and nails</p>
            <p class="text-2xl font-display font-bold text-spa-gold">${{ service.price }}</p>
          </div>
        </div>
      </div>

      <!-- Extra Services -->
      <div>
        <h2 class="text-2xl font-display font-semibold text-gray-900 mb-8">Extra Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div v-for="service in extraServices" :key="service.name" 
               class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
            <div class="flex items-center">
              <div class="flex items-center justify-center w-12 h-12 bg-spa-pink rounded-full">
                <component :is="service.icon" class="w-6 h-6 text-spa-gold" />
              </div>
              <div class="ml-4">
                <h3 class="text-xl font-display font-semibold text-gray-900">{{ service.name }}</h3>
                <p class="text-gray-600">{{ service.description }}</p>
              </div>
              <p class="ml-auto text-xl font-display font-bold text-spa-gold">${{ service.price }}</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Service Note -->
      <div class="mt-16 bg-spa-pink rounded-lg p-6 text-center">
        <p class="text-gray-800">
          All services include a complimentary consultation to ensure we understand your pet's needs.
          <br>Additional charges may apply for extra-large breeds or special conditions.
        </p>
      </div>
    </div>
  </main>
</template>

<script setup>
import { 
  SparklesIcon, 
  ScissorsIcon 
} from '@heroicons/vue/24/outline'

const basicServices = [
  { type: 'Small Dogs', price: 45 },
  { type: 'Medium Dogs', price: 55 },
  { type: 'Large Dogs', price: 65 }
]

const extraServices = [
  {
    name: 'Pet Dyeing',
    description: 'Safe, temporary color treatments',
    price: 30,
    icon: SparklesIcon
  },
  {
    name: 'Bow/Accessory',
    description: 'Stylish finishing touches',
    price: 15,
    icon: ScissorsIcon
  }
]
</script>