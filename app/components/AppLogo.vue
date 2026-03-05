<template>
  <span
    class="font-bold text-xl tracking-tight"
    :class="inverse ? 'text-white' : 'text-highlighted'"
  >
    Spa<span :class="inverse ? 'text-primary-300' : 'text-primary-600 dark:text-primary-400'">Supreme</span>
  </span>
</template>

<script setup lang="ts">
defineProps<{
  inverse?: boolean
}>()
</script>
