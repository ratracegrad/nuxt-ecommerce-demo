<script setup>
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'SpaSupreme - Premium Wellness Supplements'
const description = 'Clean, trustworthy wellness supplements for a healthier you. Natural ingredients, no harsh chemicals, designed for your wellness journey.'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/og-image.png',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <UApp class="min-h-screen flex flex-col bg-gray-50 dark:bg-gray-950">
    <NuxtLoadingIndicator />
    <AppHeader />

    <UMain>
      <NuxtPage />
    </UMain>

    <AppFooter />
  </UApp>
</template>
