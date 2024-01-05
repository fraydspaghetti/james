<script setup> const FacebookLink = 'https://www.facebook.com/nogames231/';
import MainLayout from '../components/MainLayout.vue';

// Page Title of Views
const pageTitle = 'Contact'
</script>

<template>
  <MainLayout :pageTitle="pageTitle">
    <section class="bg-gray-900 text-white py-8">
      <div class="container mx-auto text-center">
        <p class="text-lg mb-4">
         Reach me out through my social media accounts and ring me in my contacts!
        </p>
      </div>
    </section>

    <div class="max-w-full w-full bg-white p-8 rounded-lg shadow-md mx-auto mt-8">
      <h2 class="text-3xl font-bold text-cyan-800 mb-6">Get in Touch</h2>

      <form @submit.prevent="submitForm">
        <div class="mb-4">
          <div>
            <h3 class="text-lg font-semibold text-gray-800 mb-2">My Facebook:</h3>
            <a href="https://www.facebook.com/nogames231" target="_blank" class="text-blue-500 underline hover:text-blue-700">https://www.facebook.com/nogames231</a>
          </div>

          <div class="mt-4">
            <h3 class="text-lg font-semibold text-gray-800 mb-2">My Contact Number:</h3>
            <p class="text-gray-600">09336023813</p>
          </div>

          
        </div>
      </form>
    </div>
  </MainLayout>
</template>
