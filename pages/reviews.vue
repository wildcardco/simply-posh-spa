<template>
  <section class="min-h-screen bg-white py-16">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-display font-bold text-center text-gray-900 mb-8">Client Reviews</h1>
      <p class="text-center text-gray-600 mb-12">
        See what our happy clients have to say about their Simply Posh experience!
      </p>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(review, index) in reviews"
          :key="index"
          class="bg-spa-pink p-6 rounded-lg shadow-md"
        >
          <div class="flex items-center mb-4">
            <div class="h-12 w-12 rounded-full bg-spa-gold flex items-center justify-center">
              <span class="text-white text-xl font-bold">{{ review.initial }}</span>
            </div>
            <div class="ml-4">
              <h3 class="text-lg font-semibold text-gray-900">{{ review.name }}</h3>
              <p class="text-sm text-gray-600">{{ review.pet }}</p>
            </div>
          </div>
          <p class="text-gray-800">{{ review.quote }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const reviews = [
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
  },
  {
    name: 'David Lee',
    pet: 'Owner of Charlie',
    initial: 'D',
    quote: 'Charlie loves his spa days at Simply Posh! The staff is so friendly and professional. Highly recommend!'
  },
  {
    name: 'Jessica Brown',
    pet: 'Owner of Daisy',
    initial: 'J',
    quote: 'Daisy always looks stunning after her grooming sessions. The team truly cares about the pets they work with.'
  },
  {
    name: 'Chris Wilson',
    pet: 'Owner of Oliver',
    initial: 'C',
    quote: 'Oliver has never been happier! The grooming services are top-notch, and the staff is incredibly kind.'
  }
]
</script>

<style scoped>
/* Add any additional custom styles if needed */
</style>