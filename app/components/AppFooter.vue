<template>
  <UFooter
    class="bg-gray-900 text-white dark:bg-default dark:text-default"
    :ui="{ top: 'border-b border-gray-800' }"
  >
    <template #top>
      <UContainer>
        <UFooterColumns :columns="columns">
          <template #left>
            <div class="space-y-4">
              <h3 class="text-lg font-semibold">
                Feel the difference. Naturally.
              </h3>
              <p class="text-sm">
                Join thousands who've transformed their wellness with SpaSupreme.
              </p>
              <form
                class="flex gap-2"
                @submit.prevent="subscribe"
              >
                <UInput
                  v-model="email"
                  type="email"
                  placeholder="Enter your email"
                  class="flex-1 bg-gray-800 border-gray-700 text-white placeholder:text-gray-500 rounded-lg"
                  size="md"
                />
                <UButton
                  type="submit"
                  label="Join"
                  color="primary"
                  size="md"
                  class="rounded-lg shrink-0"
                />
              </form>
            </div>
            <div class="space-y-4 mt-8">
              <h4 class="text-lg font-semibold">
                Contact
              </h4>
              <address>
                <p>SpaSupreme Inc.</p>
                <p>123 Wellness Ave</p>
                <p>San Francisco, CA 94102</p>
              </address>
            </div>
          </template>

          <template #default />
        </UFooterColumns>
      </UContainer>
    </template>

    <template #left>
      <div class="flex flex-wrap justify-center lg:justify-start gap-4 text-sm">
        <ULink
          to="#"
        >
          Privacy Policy
        </ULink>
        <ULink
          to="#"
        >
          Terms of Service
        </ULink>
      </div>
    </template>

    <template #default>
      <p class="text-sm">
        © {{ new Date().getFullYear() }} SpaSupreme. All rights reserved.
      </p>
    </template>

    <template #right>
      <AppLogo />
    </template>
  </UFooter>
</template>

<script setup lang="ts">
const columns = [
  {
    label: 'Discover',
    children: [
      { label: 'Products', to: '#products' },
      { label: 'Science', to: '#science' },
      { label: 'Reviews', to: '#reviews' },
      { label: 'FAQ', to: '#faq' }
    ]
  },
  {
    label: 'Support',
    children: [
      { label: 'Contact Us', to: '#' },
      { label: 'Shipping', to: '#' },
      { label: 'Returns', to: '#' },
      { label: 'Track Order', to: '#' }
    ]
  },
  {
    label: 'Company',
    children: [{
      label: 'About'
    }, {
      label: 'Pricing'
    }, {
      label: 'Careers'
    }, {
      label: 'Blog'
    }
    ]
  }
]

const email = ref('')

function subscribe() {
  // Placeholder for newsletter subscription
  email.value = ''
}
</script>
