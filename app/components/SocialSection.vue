<template>
  <UPageSection
    id="reviews"
    title="Loved by thousands"
    description="Real results from real people. Join our community of wellness enthusiasts."
    orientation="vertical"
    class="bg-primary-50"
  >
    <UPageGrid>
      <div
        v-for="i in 3"
        :key="i"
        class="relative aspect-3/4 rounded-2xl overflow-hidden bg-gray-100 group"
      >
        <div class="absolute inset-0 bg-linear-to-t from-black/70 to-transparent" />
        <div class="absolute inset-0 flex items-center justify-center">
          <UButton
            icon="i-lucide-play"
            color="neutral"
            variant="ghost"
            class="rounded-full size-16 text-white hover:bg-white/20"
          />
        </div>
        <div class="absolute bottom-0 left-0 right-0 p-6 text-white">
          <p class="font-medium">
            Customer story {{ i }}
          </p>
          <p class="text-sm text-white/80">
            Watch their journey
          </p>
        </div>
      </div>
    </UPageGrid>
  </UPageSection>
</template>
