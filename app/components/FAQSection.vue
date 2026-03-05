<template>
  <UPageSection
    id="faq"
    title="Frequently asked questions"
    orientation="vertical"
  >
    <template #body>
      <UAccordion
        :items="faqItems"
        class="max-w-3xl mx-auto"
      />
    </template>
  </UPageSection>
</template>

<script setup lang="ts">
const faqItems = [
  {
    label: 'How long until I see results?',
    content: 'Most customers notice a difference within 2-4 weeks of consistent use. Individual results may vary based on your body and routine.'
  },
  {
    label: 'Are your supplements third-party tested?',
    content: 'Yes. Every batch is tested by independent labs for purity, potency, and safety. We share our certificates of analysis upon request.'
  },
  {
    label: 'What is your return policy?',
    content: 'We offer a 30-day money-back guarantee. If you\'re not satisfied, return the product for a full refund—no questions asked.'
  }
]
</script>
