<template>
  <UPageSection
    id="products"
    title="Choose Your Flavor"
    description="Find the perfect protein shake flavor for your wellness goals."
    orientation="vertical"
    class="bg-primary-100 dark:bg-default"
  >
    <template #body>
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <UPageCard
          v-for="product in products"
          :key="product.id"
          variant="subtle"
          class="rounded-xl shadow-lg overflow-hidden group hover:ring-2 hover:ring-primary-200 transition-all"
        >
          <div class="aspect-square overflow-hidden">
            <img
              :src="product.image"
              :alt="product.name"
              class="w-full h-full object-cover"
            >
          </div>
          <template #body>
            <h3 class="font-semibold text-gray-900">
              {{ product.name }}
            </h3>
            <p class="text-sm ">
              {{ product.description }}
            </p>
            <UButton
              to="#"
              color="neutral"
              variant="solid"
              size="sm"
              class="mt-4 w-full rounded-lg"
            >
              Shop {{ product.name }}
            </UButton>
          </template>
        </UPageCard>
      </div>
    </template>
  </UPageSection>
</template>

<script setup lang="ts">
const products = [
  {
    id: 1,
    name: 'Chocolate',
    description: 'Velvety cocoa flavor that feels indulgent.',
    image: '/flavor1.jpg'
  },
  {
    id: 2,
    name: 'Lemon',
    description: 'Sunny citrus taste, light and invigorating.',
    image: '/flavor2.jpg'
  },
  {
    id: 3,
    name: 'Vanilla',
    description: 'Subtle, smooth vanilla that works with everything."',
    image: '/flavor3.jpg'
  },
  {
    id: 4,
    name: 'Mocha',
    description: 'A rich, creamy blend of chocolate and coffee.',
    image: '/flavor4.jpg'
  }
]
</script>
