<template>
  <UPageSection
    title="Clean formulas, real results"
    description="Each product is crafted with the same care and precision we'd want for our own families."
    orientation="vertical"
  >
    <template #body>
      <div class="space-y-16 md:space-y-24">
        <UPageSection
          v-for="(feature, i) in featureProducts"
          :key="feature.name"
          orientation="horizontal"
          :reverse="i % 2 === 1"
        >
          <template #body>
            <div class="space-y-6">
              <UBadge
                color="secondary"
                variant="soft"
                size="sm"
                class="rounded-full"
              >
                {{ feature.badge }}
              </UBadge>
              <h3 class="text-2xl sm:text-3xl font-bold">
                {{ feature.name }}
              </h3>
              <p class="text-lg">
                {{ feature.description }}
              </p>
              <div class="flex flex-wrap gap-2">
                <UBadge
                  v-for="chip in feature.chips"
                  :key="chip"
                  color="neutral"
                  variant="subtle"
                  size="sm"
                >
                  {{ chip }}
                </UBadge>
              </div>
              <UButton
                to="#"
                color="neutral"
                variant="solid"
                size="lg"
                class="rounded-full"
              >
                Learn More
              </UButton>
            </div>
          </template>
          <template #default>
            <div class="relative w-full max-w-sm aspect-square rounded-2xl overflow-hidden">
              <div
                class="absolute inset-0 flex items-center justify-center"
                :class="feature.bgClass"
              >
                <div
                  class="w-40 h-52 rounded-xl shadow-xl"
                  :class="feature.colorClass"
                />
                <div class="absolute bottom-4 right-4">
                  <UIcon
                    name="i-lucide-leaf"
                    class="size-12"
                    :class="feature.colorClass"
                  />
                </div>
              </div>
            </div>
          </template>
        </UPageSection>
      </div>
    </template>
  </UPageSection>
</template>

<script setup lang="ts">
const featureProducts = [
  {
    name: 'Daily Energy Complex',
    badge: 'Best Seller',
    description: 'A clinically studied blend of vitamins and adaptogens designed to support sustained energy throughout your day. No jitters, no crash—just steady, natural vitality.',
    chips: ['B vitamins', 'Ashwagandha', 'No caffeine crash'],
    bgClass: 'bg-primary-100/50',
    colorClass: 'bg-primary-500/80'
  },
  {
    name: 'Rest & Restore',
    badge: 'Natural',
    description: 'Promote deeper sleep with our melatonin-free formula. Magnesium, L-theanine, and calming botanicals help you wind down and wake up refreshed.',
    chips: ['Magnesium', 'L-theanine', 'Non-habit forming'],
    bgClass: 'bg-secondary-100/50',
    colorClass: 'bg-secondary-500/80'
  }
]
</script>
