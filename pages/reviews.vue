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
            <div class="h-12 w-12 rounded-full overflow-hidden bg-gray-200 flex items-center justify-center">
              <img
                v-if="review.image"
                :src="review.image"
                alt="Photo of {{ review.name }}"
                class="h-full w-full object-cover"
              />
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
    name: 'Brenda S.',
    pet: 'Owner of Max',
    image: '/images/BrendaMax.jpg',
    quote: 'AMAZING!!!!! I was super scared on where to take my baby Max to get groomed for his first time but she made us feel right at home!!! My Maxy came home super content and relaxed!!!!! This is the only place Max will be going to!!!! <3 '
  },
  {
    name: 'Mari S.',
    pet: 'Owner of Princess',
    image: 'images/MariPrincess.jpg',
    quote: 'Our baby mini poodle always gets a Princess treatment! She comes out smelling and looking amazing; I highly recommend simply posh!'
  },
  {
    name: 'Cindy Aviles',
    pet: 'Owner of Snow',
    image: 'images/CindyDog.jpg',
    quote: 'She was great with our standard poodle! He has gone twice and he looked absolutely beautiful both times! She takes her time with your pet to ensure that they are comfortable :) Definitely recommend!'
  }

]
</script>

<style scoped>
/* Add any additional custom styles if needed */
</style>