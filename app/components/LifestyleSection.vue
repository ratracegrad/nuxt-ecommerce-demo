<template>
  <UPageSection
    title="Designed for real life"
    description="Our supplements fit seamlessly into your daily routine. Simple, effective, and made for the way you actually live."
    orientation="horizontal"
  >
    <template #headline>
      <UBadge
        color="secondary"
        variant="soft"
        size="sm"
        class="rounded-full"
      >
        Start Your Journey
      </UBadge>
    </template>
    <template #body>
      <ul class="space-y-3">
        <li
          v-for="item in lifestyleBenefits"
          :key="item"
          class="flex items-center gap-3 text-gray-700"
        >
          <UIcon
            name="i-lucide-check"
            class="size-5 text-secondary-500 shrink-0"
          />
          <span>{{ item }}</span>
        </li>
      </ul>
    </template>

    <template #default>
      <div class="relative aspect-[4/3] rounded-2xl overflow-hidden bg-gray-100">
        <div class="absolute inset-0 flex items-center justify-center">
          <div class="w-48 h-64 rounded-2xl bg-gradient-to-br from-primary-300 to-primary-600 shadow-2xl" />
        </div>
      </div>
    </template>
  </UPageSection>
</template>

<script setup lang="ts">
const lifestyleBenefits = [
  'Ease of digestion',
  'No bloating',
  'No harsh chemicals',
  'No crash energy',
  'Cleaner formula'
]
</script>
