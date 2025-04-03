<template>
  <section class="min-h-screen bg-gray-50 py-12">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold text-center text-gray-800 mb-8">Contact Us</h1>
      <p class="text-center text-gray-600 mb-12">
        Have questions or need assistance? Fill out the form below, and we'll get back to you as soon as possible.
      </p>
      <div class="max-w-2xl mx-auto shadow-md rounded-lg p-8">
        <form @submit.prevent="submitForm">
          <div class="mb-6">
            <label for="name" class="block text-sm font-medium text-gray-700">Name</label>
            <input
              type="text"
              id="name"
              v-model="form.name"
              class="mt-1 block w-full rounded-md border border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 bg-transparent"
              placeholder="Your Name"
              required
            />
          </div>
          <div class="mb-6">
            <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
            <input
              type="email"
              id="email"
              v-model="form.email"
              class="mt-1 block w-full rounded-md border border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 bg-transparent"
              placeholder="Your Email"
              required
            />
          </div>
          <div class="mb-6">
            <label for="message" class="block text-sm font-medium text-gray-700">Message</label>
            <textarea
              id="message"
              v-model="form.message"
              rows="4"
              class="mt-1 block w-full rounded-md border border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 bg-transparent"
              placeholder="Your Message"
              required
            ></textarea>
          </div>
          <div class="text-center">
            <button
              type="submit"
              class="inline-flex justify-center w-full bg-indigo-600 text-white font-medium py-2 px-4 rounded-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
            >
              Send Message
            </button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup>
// Reactive form data
import { reactive } from 'vue';

const form = reactive({
  name: '',
  email: '',
  message: '',
});

const submitForm = () => {
  alert(`Thank you, ${form.name}! Your message has been sent.`);
  // Reset form fields
  form.name = '';
  form.email = '';
  form.message = '';
};
</script>

<style scoped>
/* Ensure the button is visible */
button {
  display: inline-flex;
  visibility: visible;
}

/* Remove any conflicting styles */
form {
  background: transparent;
}

input,
textarea {
  background: transparent;
}
</style>