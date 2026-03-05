<template>
  <UPageSection
    title="Join us @SpaSupreme"
    description="Share your wellness journey. Tag us for a chance to be featured."
    orientation="vertical"
    :links="[{ label: 'Follow on Instagram', to: '#', target: '_blank', color: 'secondary', size: 'lg', class: 'rounded-full' }]"
    class="bg-secondary-50"
  >
    <template #body>
      <div class="relative h-64 md:h-80 rounded-2xl overflow-hidden">
        <div class="absolute inset-0 flex items-center justify-center gap-4 p-4">
          <img
            v-for="(img, i) in joinImages"
            :key="i"
            :src="img"
            :alt="`Community photo ${i + 1}`"
            class="w-24 h-32 md:w-32 md:h-40 object-cover rounded-xl border-4 border-secondary shadow-lg"
            :class="socialCollageRotations[i % 5]"
          >
        </div>
      </div>
    </template>
  </UPageSection>
</template>

<script setup lang="ts">
const joinImages = [
  '/join1.jpg',
  '/join2.jpg',
  '/join3.jpg',
  '/join4.jpg',
  '/join5.jpg'
]

const socialCollageRotations = [
  'rotate-[-8deg] -translate-y-2',
  'rotate-[5deg] translate-y-4',
  'rotate-[-3deg]',
  'rotate-[7deg] -translate-y-1',
  'rotate-[-5deg] translate-y-2'
]
</script>
