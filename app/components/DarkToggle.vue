<script setup lang="ts">
import { useColorMode } from '@vueuse/core'

const color = useColorMode()

useHead({
  meta: [
    {
      id: 'theme-color',
      name: 'theme-color',
      content: () => (color.value === 'dark' ? '#222222' : '#ffffff'),
    },
  ],
})

function toggleDark() {
  color.value = color.value === 'dark' ? 'light' : 'dark'
}
</script>

<template>
  <button class="outline-none focus:outline-none" @click="toggleDark">
    <div
      class="w-6 h-6 transition-all duration-300"
      :class="color === 'dark' ? 'text-white' : 'text-yellow-500'"
    >
      <i v-if="color === 'dark'" class="fas fa-moon" />
      <i v-else class="fas fa-sun" />
    </div>
  </button>
</template>
