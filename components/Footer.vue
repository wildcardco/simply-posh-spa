<template>
  <footer class="bg-white mt-12">
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div>
          <h3 class="text-lg font-display font-semibold text-gray-900">Simply Posh</h3>
          <p class="mt-2 text-sm text-gray-600">Because every pet deserves to feel fabulous.</p>
        </div>
        <div>
          <h3 class="text-lg font-display font-semibold text-gray-900">Hours</h3>
          <ul class="mt-2 space-y-1 text-sm text-gray-600">
            <li>Monday - Friday: 9am - 6pm</li>
            <li>Saturday: 9am - 4pm</li>
            <li>Sunday: Closed</li>
          </ul>
        </div>
        <div>
          <h3 class="text-lg font-display font-semibold text-gray-900">Contact</h3>
          <ul class="mt-2 space-y-1 text-sm text-gray-600">
            <li>123 Pet Paradise Lane</li>
            <li>Beverly Hills, CA 90210</li>
            <li>(555) 123-4567</li>
            <li>info@simplyposhspa.com</li>
          </ul>
        </div>
      </div>
      <div class="mt-8 pt-8 border-t border-gray-200 text-center text-sm text-gray-600">
        <p>&copy; {{ new Date().getFullYear() }} Simply Posh Salon and Spa. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>