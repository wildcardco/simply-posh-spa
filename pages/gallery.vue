<template>
  <main class="py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h1 class="text-4xl font-display font-bold text-center text-gray-900 mb-12">Before & After Gallery</h1>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(transformation, index) in transformations" :key="index" class="bg-white rounded-lg shadow-sm overflow-hidden">
          <div class="relative">
            <div class="aspect-w-4 aspect-h-3">
              <img :src="transformation.before" alt="Before transformation" class="object-cover">
            </div>
            <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent flex items-end">
              <span class="text-white font-medium p-4">Before</span>
            </div>
          </div>
          <div class="relative">
            <div class="aspect-w-4 aspect-h-3">
              <img :src="transformation.after" alt="After transformation" class="object-cover">
            </div>
            <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent flex items-end">
              <span class="text-white font-medium p-4">After</span>
            </div>
          </div>
          <div class="p-4">
            <h3 class="font-display font-semibold text-gray-900">{{ transformation.name }}</h3>
            <p class="text-gray-600 text-sm mt-1">{{ transformation.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
const transformations = [
  {
    name: '',
    description: '',
    before: 'images/BeforeSmoky.jpg',
    after: 'images/AfterSmoky.jpg'
  },
  {
    name: '',
    description: '',
    before: 'images/BeforeSunny.jpg',
    after: 'images/AfterSunny.jpg'
  },
  {
    name: '',
    description: '',
    before: 'images/BeforeSnowy.png',
    after: 'images/AfterSnowy.png'
  },
  {
    name: '',
    description: '',
    before: 'images/BeforeBrownie.png',
    after: 'images/AfterBrownie.png'
  },
  {
    name: '',
    description: '',
    before: 'images/BeforeCupcake.png',
    after: 'images/AfterCupcake.png'
  },
  {
    name: '',
    description: '',
    before: 'images/BeforeLucy.png',
    after: 'images/AfterLucy.png'
  }
]
</script>