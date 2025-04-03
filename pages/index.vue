<template>
  <main>
    <!-- Hero Section -->
    <div class="relative bg-spa-pink">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <div class="text-center">
          <h1 class="text-4xl tracking-tight font-display font-bold text-gray-900 sm:text-5xl md:text-6xl">
            <span class="block">Welcome to Simply Posh</span>
            <span class="block text-spa-gold">Salon and Spa</span>
          </h1>
          <p class="mt-3 max-w-md mx-auto text-base text-gray-600 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">
            Because every pet deserves to feel fabulous
          </p>
          <div class="mt-5 max-w-md mx-auto sm:flex sm:justify-center md:mt-8">
            <div class="rounded-md shadow">
              <NuxtLink
                to="/services"
                class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-spa-gold hover:bg-opacity-90 md:py-4 md:text-lg md:px-10"
              >
                View Our Services
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Mission Section -->
    <div class="py-16 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h2 class="text-3xl font-display font-bold text-gray-900">Our Mission</h2>
          <p class="mt-4 max-w-2xl mx-auto text-xl text-gray-600">
            At Simply Posh, we believe that every pet deserves the highest quality care and pampering. 
            Our expert groomers provide compassionate, luxury services tailored to each pet's unique needs.
          </p>
        </div>
      </div>
    </div>

    <!-- Featured Testimonials -->
    <div class="bg-spa-gray py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-display font-bold text-center text-gray-900 mb-12">What Our Clients Say</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="(testimonial, index) in testimonials" :key="index" class="bg-white p-6 rounded-lg shadow-sm">
            <div class="flex items-center mb-4">
              <div class="h-12 w-12 rounded-full bg-spa-pink flex items-center justify-center">
                <span class="text-spa-gold text-xl">{{ testimonial.initial }}</span>
              </div>
              <div class="ml-4">
                <h3 class="text-lg font-semibold text-gray-900">{{ testimonial.name }}</h3>
                <p class="text-sm text-gray-600">{{ testimonial.pet }}</p>
              </div>
            </div>
            <p class="text-gray-600">{{ testimonial.quote }}</p>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
const testimonials = [
  {
    name: 'Sarah Johnson',
    pet: 'Owner of Luna',
    initial: 'S',
    quote: 'Simply Posh transformed my nervous Luna into a confident, beautiful pup. The care and attention they provide is unmatched!'
  },
  {
    name: 'Michael Chen',
    pet: 'Owner of Max',
    initial: 'M',
    quote: 'The team here is amazing! Max always comes home looking and smelling wonderful. Best grooming experience ever!'
  },
  {
    name: 'Emily Davis',
    pet: 'Owner of Bella',
    initial: 'E',
    quote: 'I wouldn\'t trust anyone else with my Bella. The attention to detail and gentle approach makes all the difference.'
  }
]
</script>