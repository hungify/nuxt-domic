<script setup lang="ts">
const { count, inc, dec } = useCount()
</script>

<template>
  <div class="inline-flex my-3">
    <button
      class="rounded-full p-2 bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 transition"
      @click="dec()"
    >
      <i class="i-carbon-add" />
    </button>
    <div class="font-mono w-15 mx-auto inline-block">
      {{ count }}
    </div>
    <button
      class="rounded-full p-2 bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 transition"
      @click="inc()"
    >
      <i class="fas fa-plus" />
    </button>
  </div>
</template>
