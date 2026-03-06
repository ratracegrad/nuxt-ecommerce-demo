<template>
  <UPageHero
    orientation="horizontal"
    description="Clean supplements formulated for real results. No harsh chemicals, no crash—just the nutrients your body needs to thrive."
    :links="links"
    class="bg-primary-100 dark:bg-default bg-radial from-primary-50 from-40% to-primary-500"
  >
    <template #headline>
      <UBadge
        color="primary"
      >
        Premium Wellness
      </UBadge>
    </template>

    <template #title>
      <h1>
        Your best self
        <span class="text-primary-600">starts here</span>
      </h1>
    </template>

    <template #body>
      <div class="flex flex-wrap gap-6">
        <div
          class="flex items-center gap-2 text-sm"
        >
          <UIcon
            name="i-lucide-truck"
            class="size-5 text-primary"
          />
          <span>Free shipping</span>
        </div>
        <div
          class="flex items-center gap-2 text-sm"
        >
          <UIcon
            name="i-lucide-shield-check"
            class="size-5 text-primary"
          />
          <span>30-day guarantee</span>
        </div>
      </div>
    </template>

    <template #default>
      <div class="flex justify-center lg:justify-end">
        <div
          class="relative w-full max-w-md aspect-square bg-primary rounded-3xl flex items-center justify-center overflow-hidden"
        >
          <div class="flex gap-4 -rotate-6">
            <div
              class="w-32 h-40 rounded-2xl shadow-lg overflow-hidden shrink-0"
            >
              <img
                src="/drink1.jpg"
                alt="SpaSupreme drink"
                class="w-full h-full object-cover border-4 border-white rounded-2xl"
              >
            </div>
            <div
              class="w-32 h-40 rounded-2xl shadow-lg overflow-hidden shrink-0 self-end"
            >
              <img
                src="/flavor1.jpg"
                alt="SpaSupreme flavor"
                class="w-full h-full object-cover border-4 border-white rounded-2xl"
              >
            </div>
            <div
              class="w-32 h-40 rounded-2xl shadow-xl overflow-hidden shrink-0 self-center"
            >
              <img
                src="/product1.jpg"
                alt="SpaSupreme product"
                class="w-full h-full object-cover border-4 border-white rounded-2xl"
              >
            </div>
          </div>
        </div>
      </div>
    </template>
  </UPageHero>
</template>

<script setup lang="ts">
import type { ButtonProps } from '@nuxt/ui'

const links = ref<ButtonProps[]>([
  {
    label: 'Shop Now',
    to: '#products',
    color: 'primary'
  },
  {
    label: 'Learn the Science',
    to: '#science',
    color: 'neutral',
    variant: 'outline'
  }
])
</script>
