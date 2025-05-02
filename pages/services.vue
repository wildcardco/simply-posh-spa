<template>
  <main class="py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h1 class="text-4xl font-display font-bold text-center text-gray-900 mb-12">Our Services</h1>

      <!-- Full Services -->
      <div class="mb-16">
        <h2 class="text-2xl font-display font-semibold text-gray-900 mb-8">Full Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="service in fullServices" :key="service.type" 
               class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
            <div class="flex items-center justify-center w-12 h-12 bg-spa-pink rounded-full mb-4">
              <svg class="w-6 h-6 text-spa-gold" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                      d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
              </svg>
            </div>
            <h3 class="text-xl font-display font-semibold text-gray-900 mb-2">{{ service.type }}</h3>
            <p class="text-gray-600 mb-4">Includes optional Spa Package, groom of choice, nail trim, and an ear cleaning.</p>
            <p class="text-4xl font-display font-bold text-spa-gold">${{ service.price }}</p>
          </div>
        </div>
      </div>

      <!-- Alternate Services -->
      <div class="mb-16">
        <h2 class="text-2xl font-display font-semibold text-gray-900 mb-8">Alternate Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="service in alternateServices" :key="service.type" 
               class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
            <div class="flex items-center justify-center w-12 h-12 bg-spa-pink rounded-full mb-4">
              <svg class="w-6 h-6 text-spa-gold" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                      d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
              </svg>
            </div>
            <h3 class="text-xl font-display font-semibold text-gray-900 mb-2">{{ service.type }}</h3>
            <p class="text-gray-600 mb-4">Includes optional Spa Package, nail/paw trim, and face cleaning.</p>
            <p class="text-4xl font-display font-bold text-spa-gold">${{ service.price }}</p>
          </div>
        </div>
      </div>

      <!-- Short Hair Services -->
      <div class="mb-16">
        <h2 class="text-2xl font-display font-semibold text-gray-900 mb-8">Short Hair Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="service in shorthairServices" :key="service.type" 
               class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
            <div class="flex items-center justify-center w-12 h-12 bg-spa-pink rounded-full mb-4">
              <svg class="w-6 h-6 text-spa-gold" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                      d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
              </svg>
            </div>
            <h3 class="text-xl font-display font-semibold text-gray-900 mb-2">{{ service.type }}</h3>
            <p class="text-gray-600 mb-4">Includes optional Spa Package, nail trim, Hair Brush, and ear cleaning.</p>
            <p class="text-4xl font-display font-bold text-spa-gold">${{ service.price }}</p>
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
              <p class="ml-auto text-4xl font-display font-bold text-spa-gold">${{ service.price }}</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Service Note -->
      <div class="mt-16 bg-spa-pink rounded-lg p-6 text-center">
        <p class="text-gray-800">
          All services include a complimentary consultation to ensure we understand your pet's needs. Spa Package includes: Deep Conditioning Treatment, Deshed, Blueberry Facial, Pawdicure, teeth brushing, Medicated or flea shampoo, and an anal gland expression. 
          <br>
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

const fullServices = [
  { type: 'Full Groom for Small Dogs', price: 45 },
  { type: 'Full Groom for Medium Dogs', price: 55 },
  { type: 'Full Groom for Large Dogs', price: 65 },
  { type: 'Full Groom for Extra Large Dogs', price: 75 },
]

const alternateServices = [
  { type: 'Face, Feet, and Tail Groom for Small Dogs', price: 30 },
  { type: 'Face, Feet, and Tail Groom for Medium Dogs', price: 40 },
  { type: 'Face, Feet, and Tail Groom for Large Dogs', price: 50},
  { type: 'Face, Feet, and Tail Groom for Extra Large Dogs', price: 60 },
]

const shorthairServices = [
  { type: 'Short Hair Groom for Small Dogs', price: 30 },
  { type: 'Short Hair Groom for Medium Dogs', price: 40 },
  { type: 'Short Hair Groom for Large Dogs', price: 50 },
  { type: 'Short Hair Groom for Extra Large Dogs', price: 60 },
]

const extraServices = [
  {
    name: 'Full Brush and Comb Out',
    description: '',
    price: 10,
    icon: SparklesIcon
  },
  {
    name: 'Silky Press flat-iron Treatment',
    description: '',
    price: 5,
    icon: SparklesIcon
  },
  {
    name: 'Semi-permanent Pet Dye',
    description: 'Add a pop of color to your pet\'s coat!',
    price: 5,
    icon: SparklesIcon
  },
  {
    name: 'Nail polish',
    description: '',
    price: 5,
    icon: SparklesIcon
  },
  {
    name: 'Free Nail Trims For Customers! (Please call or text to schedule in advance.)',
    description: '',
    price: 0,
    icon: ScissorsIcon
  }
]
</script>