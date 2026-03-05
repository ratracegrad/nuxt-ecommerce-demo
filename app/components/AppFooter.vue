<template>
  <footer class="bg-gray-900 text-white">
    <UContainer class="py-16 md:py-20">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 lg:gap-16">
        <!-- Left: Product promise + newsletter -->
        <div class="lg:col-span-1 space-y-6">
          <h3 class="text-lg font-bold text-white">
            Feel the difference. Naturally.
          </h3>
          <p class="text-sm text-gray-400">
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

        <!-- Discover -->
        <div>
          <h4 class="text-sm font-semibold text-white uppercase tracking-wider mb-4">
            Discover
          </h4>
          <ul class="space-y-3">
            <li>
              <ULink
                to="#products"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Products</ULink>
            </li>
            <li>
              <ULink
                to="#science"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Science</ULink>
            </li>
            <li>
              <ULink
                to="#reviews"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Reviews</ULink>
            </li>
            <li>
              <ULink
                to="#faq"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >FAQ</ULink>
            </li>
          </ul>
        </div>

        <!-- Support -->
        <div>
          <h4 class="text-sm font-semibold text-white uppercase tracking-wider mb-4">
            Support
          </h4>
          <ul class="space-y-3">
            <li>
              <ULink
                to="#"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Contact Us</ULink>
            </li>
            <li>
              <ULink
                to="#"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Shipping</ULink>
            </li>
            <li>
              <ULink
                to="#"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Returns</ULink>
            </li>
            <li>
              <ULink
                to="#"
                class="text-gray-400 hover:text-white text-sm transition-colors"
              >Track Order</ULink>
            </li>
          </ul>
        </div>

        <!-- Contact -->
        <div>
          <h4 class="text-sm font-semibold text-white uppercase tracking-wider mb-4">
            Contact
          </h4>
          <address class="text-gray-400 text-sm not-italic space-y-1">
            <p>SpaSupreme Inc.</p>
            <p>123 Wellness Ave</p>
            <p>San Francisco, CA 94102</p>
          </address>
        </div>
      </div>

      <!-- Bottom row -->
      <div class="mt-16 pt-8 border-t border-gray-800 flex flex-col md:flex-row items-center justify-between gap-4">
        <div class="flex flex-wrap justify-center md:justify-start gap-4 text-sm">
          <ULink
            to="#"
            class="text-gray-500 hover:text-gray-300 transition-colors"
          >Privacy Policy</ULink>
          <ULink
            to="#"
            class="text-gray-500 hover:text-gray-300 transition-colors"
          >Terms of Service</ULink>
        </div>
        <p class="text-gray-500 text-sm">
          © {{ new Date().getFullYear() }} SpaSupreme. All rights reserved.
        </p>
        <div class="shrink-0">
          <AppLogo inverse />
        </div>
      </div>
    </UContainer>
  </footer>
</template>

<script setup lang="ts">
const email = ref('')

function subscribe() {
  // Placeholder for newsletter subscription
  email.value = ''
}
</script>
