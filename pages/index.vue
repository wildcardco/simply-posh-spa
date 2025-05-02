<template>
  <main>
    <!-- Hero Section -->
    <div class="relative h-screen w-full">
      <!-- Nuxt Image for optimized background -->
      <NuxtImg
        src="images/FrontPage.jpg"
        alt="Happy dog relaxing after grooming"
        class="absolute inset-0 h-full w-full object-cover"
      />
      <!-- Overlay for blending and text readability -->
      <div class="absolute inset-0 bg-black/50"></div>
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24 flex items-center justify-center h-full">
        <div class="text-center">
          <h1 class="text-4xl tracking-tight font-display font-bold text-white sm:text-5xl md:text-6xl">
            <span class="block">Welcome to Simply Posh</span>
            <span class="block text-spa-gold">Salon and Spa</span>
          </h1>
          <p class="mt-3 max-w-md mx-auto text-base text-gray-200 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">
            Because every pet deserves a spa day.
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
            At Simply Posh Salon and Spa, we believe that every pet deserves the highest quality care and pampering. 
            We provide them with compassionate, luxury services tailored to each pet's unique needs.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
/* Ensure the Hero Section spans the full viewport */
.h-screen {
  height: 100vh;
}
</style>