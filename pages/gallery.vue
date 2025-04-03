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
    name: 'Luna - Spa Day Makeover',
    description: 'Full grooming with special attention to matted fur',
    before: 'https://images.unsplash.com/photo-1583511655857-d19b40a7a54e',
    after: 'https://images.unsplash.com/photo-1583511666407-5f06533f2113'
  },
  {
    name: 'Max - Complete Transformation',
    description: 'Thorough grooming and styling for a fresh look',
    before: 'https://images.unsplash.com/photo-1576201836106-db1758fd1c97',
    after: 'https://images.unsplash.com/photo-1587300003388-59208cc962cb'
  },
  {
    name: 'Bella - Luxury Treatment',
    description: 'Premium grooming package with fur conditioning',
    before: 'https://images.unsplash.com/photo-1517423440428-a5a00ad493e8',
    after: 'https://images.unsplash.com/photo-1517423738875-5ce310acd3da'
  },
  {
    name: 'Charlie - Style Refresh',
    description: 'Modern cut with detailed trimming',
    before: 'https://images.unsplash.com/photo-1596492784531-6e6eb5ea9993',
    after: 'https://images.unsplash.com/photo-1596492784531-6e6eb5ea9993'
  },
  {
    name: 'Daisy - Gentle Care',
    description: 'Sensitive skin treatment and styling',
    before: 'https://images.unsplash.com/photo-1558788353-f76d92427f16',
    after: 'https://images.unsplash.com/photo-1560807707-8cc77767d783'
  },
  {
    name: 'Oliver - Premium Package',
    description: 'Deluxe grooming with specialty products',
    before: 'https://images.unsplash.com/photo-1535930891776-0c2dfb7fda1a',
    after: 'https://images.unsplash.com/photo-1535930891776-0c2dfb7fda1a'
  }
]
</script>