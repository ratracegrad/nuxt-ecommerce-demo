<template>
  <UPageSection
    :ui="{ container: 'py-0' }"
    class="bg-gray-100"
  >
    <template #body>
      <div class="relative aspect-video md:aspect-21/9 overflow-hidden rounded-lg">
        <div class="absolute inset-0 bg-gray-800">
          <div class="absolute inset-0 bg-linear-to-t from-black/60 to-black/20" />
        </div>
        <div class="absolute inset-0 flex flex-col items-center justify-center gap-6">
          <UButton
            icon="i-lucide-play"
            color="neutral"
            variant="solid"
            size="xl"
            class="rounded-full size-20"
          />
          <h2 class="text-2xl sm:text-4xl font-bold text-white text-center px-4">
            The SpaSupreme Story
          </h2>
          <p class="text-white/90 text-lg max-w-2xl text-center px-4">
            Discover how we're redefining wellness, one supplement at a time.
          </p>
        </div>
      </div>
    </template>
  </UPageSection>
</template>
