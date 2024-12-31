<script setup lang="ts">
definePageMeta({
  layout: 'home',
})
</script>

<template>
  <div>
    <Logos class="mb-6" />
    <ClientOnly>
      <Suspense>
        <Counter />
        <template #fallback>
          <div class="italic opacity-50">
            <span class="animate-pulse">Loading...</span>
          </div>
        </template>
      </Suspense>
      <template #fallback>
        <div class="opacity-50">
          <span class="animate-pulse">...</span>
        </div>
      </template>
    </ClientOnly>
  </div>
</template>
