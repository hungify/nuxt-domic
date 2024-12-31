<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()
</script>

<template>
  <main class="px-4 py-10 text-center text-teal-700 dark:text-gray-200">
    <div class="text-4xl">
      <i class="fas fa-exclamation-triangle inline-block" />
    </div>
    <div>Not found</div>
    <div>
      <button
        class="mt-8 mb-3 px-4 py-2 text-sm font-medium text-white bg-teal-600 rounded-md hover:bg-teal-700 focus:outline-none focus:ring-2 focus:ring-teal-500"
        @click="router.back()"
      >
        Back
      </button>
    </div>
  </main>
</template>
