<template>
  <div>
    <!-- Promo bar -->
    <UBanner
      title="Free shipping on orders over $50 • 30-day money-back guarantee"
      color="primary"
      :close="false"
    />

    <!-- Main navigation -->
    <UHeader>
      <template #left>
        <NuxtLink
          to="/"
          class="flex items-center shrink-0"
        >
          <AppLogo class="w-auto h-6 shrink-0" />
        </NuxtLink>
      </template>

      <UNavigationMenu
        :items="navItems"
        variant="link"
      />

      <template #right>
        <UColorModeButton class="hidden sm:inline-flex" />
        <UButton
          to="#products"
          label="Shop Now"
          color="primary"
          class="hidden md:inline-flex"
        />
      </template>

      <template #body>
        <UNavigationMenu
          :items="navItems"
          orientation="vertical"
          class="-mx-2.5"
        />

        <USeparator class="my-6" />

        <UButton
          to="#products"
          label="Shop Now"
          color="primary"
          block
          class="rounded-full"
        />
      </template>
    </UHeader>
  </div>
</template>

<script setup lang="ts">
const navItems = [
  { label: 'Products', to: '#products' },
  { label: 'Science', to: '#science' },
  { label: 'Reviews', to: '#reviews' },
  { label: 'FAQ', to: '#faq' }
]
</script>
