<template>
  <div>
    <HeroSection />

    <!-- Benefits section -->
    <section
      id="science"
      class="py-16 md:py-24 bg-white dark:bg-gray-950"
    >
      <UContainer>
        <div class="text-center max-w-3xl mx-auto mb-12 md:mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Why SpaSupreme?
          </h2>
          <p class="text-gray-600 dark:text-gray-400 text-lg">
            We combine clinical-grade ingredients with natural wellness to deliver results you can feel.
          </p>
        </div>
        <div class="grid md:grid-cols-3 gap-8">
          <UCard
            variant="outline"
            class="rounded-xl"
          >
            <template #header>
              <div class="flex items-start gap-4">
                <div class="p-2 rounded-lg bg-secondary-100 dark:bg-secondary-900/40">
                  <UIcon
                    name="i-lucide-leaf"
                    class="size-6 text-secondary-600 dark:text-secondary-400"
                  />
                </div>
                <div>
                  <UBadge
                    color="secondary"
                    variant="soft"
                    size="xs"
                    class="rounded-full mb-2"
                  >
                    Natural
                  </UBadge>
                  <h3 class="font-semibold text-lg text-gray-900 dark:text-white">
                    Clean Ingredients
                  </h3>
                </div>
              </div>
            </template>
            <p class="text-gray-600 dark:text-gray-400">
              No artificial fillers, no harsh chemicals. Every ingredient is selected for purity and efficacy.
            </p>
          </UCard>
          <UCard
            variant="outline"
            class="rounded-xl"
          >
            <template #header>
              <div class="flex items-start gap-4">
                <div class="p-2 rounded-lg bg-primary-100 dark:bg-primary-900/40">
                  <UIcon
                    name="i-lucide-flask-conical"
                    class="size-6 text-primary-600 dark:text-primary-400"
                  />
                </div>
                <div>
                  <h3 class="font-semibold text-lg text-gray-900 dark:text-white">
                    Science-Backed
                  </h3>
                </div>
              </div>
            </template>
            <p class="text-gray-600 dark:text-gray-400">
              Formulated with clinically studied doses. We prioritize what works, not what sells.
            </p>
          </UCard>
          <UCard
            variant="outline"
            class="rounded-xl"
          >
            <template #header>
              <div class="flex items-start gap-4">
                <div class="p-2 rounded-lg bg-secondary-100 dark:bg-secondary-900/40">
                  <UIcon
                    name="i-lucide-heart"
                    class="size-6 text-secondary-600 dark:text-secondary-400"
                  />
                </div>
                <div>
                  <UBadge
                    color="secondary"
                    variant="soft"
                    size="xs"
                    class="rounded-full mb-2"
                  >
                    Gentle
                  </UBadge>
                  <h3 class="font-semibold text-lg text-gray-900 dark:text-white">
                    Easy on Your Body
                  </h3>
                </div>
              </div>
            </template>
            <p class="text-gray-600 dark:text-gray-400">
              No bloating, no crash. Our formulas are designed for daily use without harsh side effects.
            </p>
          </UCard>
        </div>
      </UContainer>
    </section>

    <!-- Plans / Product grid -->
    <section
      id="products"
      class="py-16 md:py-24 bg-gray-50 dark:bg-gray-900/50"
    >
      <UContainer>
        <div class="text-center max-w-3xl mx-auto mb-12 md:mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Choose Your Plan
          </h2>
          <p class="text-gray-600 dark:text-gray-400 text-lg">
            Find the perfect supplement routine for your wellness goals.
          </p>
        </div>
        <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
          <UCard
            v-for="product in products"
            :key="product.id"
            variant="subtle"
            class="rounded-xl overflow-hidden group hover:ring-2 hover:ring-primary-200 dark:hover:ring-primary-800 transition-all"
          >
            <div
              class="aspect-square flex items-center justify-center p-8"
              :class="product.bgClass"
            >
              <div
                class="w-24 h-32 rounded-xl shadow-md"
                :class="product.colorClass"
              />
            </div>
            <template #body>
              <h3 class="font-semibold text-gray-900 dark:text-white">
                {{ product.name }}
              </h3>
              <p class="text-sm text-gray-600 dark:text-gray-400 mt-1">
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
          </UCard>
        </div>
      </UContainer>
    </section>

    <!-- Lifestyle split section -->
    <section class="py-16 md:py-24 bg-white dark:bg-gray-950">
      <UContainer>
        <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
          <div class="space-y-6">
            <UBadge
              color="secondary"
              variant="soft"
              size="sm"
              class="rounded-full"
            >
              Start Your Journey
            </UBadge>
            <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">
              Designed for real life
            </h2>
            <p class="text-gray-600 dark:text-gray-400 text-lg">
              Our supplements fit seamlessly into your daily routine. Simple, effective, and made for the way you actually live.
            </p>
            <ul class="space-y-3">
              <li
                v-for="item in lifestyleBenefits"
                :key="item"
                class="flex items-center gap-3 text-gray-700 dark:text-gray-300"
              >
                <UIcon
                  name="i-lucide-check"
                  class="size-5 text-secondary-500 shrink-0"
                />
                <span>{{ item }}</span>
              </li>
            </ul>
          </div>
          <div class="relative aspect-[4/3] rounded-2xl overflow-hidden bg-gray-100 dark:bg-gray-800">
            <div class="absolute inset-0 flex items-center justify-center">
              <div class="w-48 h-64 rounded-2xl bg-gradient-to-br from-primary-300 to-primary-600 dark:from-primary-700 dark:to-primary-900 shadow-2xl" />
            </div>
          </div>
        </div>
      </UContainer>
    </section>

    <!-- Video section -->
    <section class="py-0">
      <div class="relative aspect-video md:aspect-[21/9] overflow-hidden">
        <div class="absolute inset-0 bg-gray-800">
          <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-black/20" />
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
    </section>

    <!-- Feature products section -->
    <section class="py-16 md:py-24 bg-gray-50 dark:bg-gray-900/50">
      <UContainer>
        <div class="text-center max-w-3xl mx-auto mb-12 md:mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Clean formulas, real results
          </h2>
          <p class="text-gray-600 dark:text-gray-400 text-lg">
            Each product is crafted with the same care and precision we'd want for our own families.
          </p>
        </div>
        <div class="space-y-16 md:space-y-24">
          <div
            v-for="(feature, i) in featureProducts"
            :key="feature.name"
            class="grid lg:grid-cols-2 gap-12 items-center"
            :class="{ 'lg:flex-row-reverse': i % 2 === 1 }"
          >
            <div
              class="flex justify-center order-2"
              :class="i % 2 === 1 ? 'lg:order-2' : 'lg:order-1'"
            >
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
                      class="size-12 text-secondary-400/50"
                    />
                  </div>
                </div>
              </div>
            </div>
            <div
              class="space-y-6 order-1"
              :class="i % 2 === 1 ? 'lg:order-1' : 'lg:order-2'"
            >
              <UBadge
                color="secondary"
                variant="soft"
                size="sm"
                class="rounded-full"
              >
                {{ feature.badge }}
              </UBadge>
              <h3 class="text-2xl sm:text-3xl font-bold text-gray-900 dark:text-white">
                {{ feature.name }}
              </h3>
              <p class="text-gray-600 dark:text-gray-400 text-lg">
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
          </div>
        </div>
      </UContainer>
    </section>

    <!-- Social proof / testimonials -->
    <section
      id="reviews"
      class="py-16 md:py-24 bg-white dark:bg-gray-950"
    >
      <UContainer>
        <div class="text-center max-w-3xl mx-auto mb-12 md:mb-16">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Loved by thousands
          </h2>
          <p class="text-gray-600 dark:text-gray-400 text-lg">
            Real results from real people. Join our community of wellness enthusiasts.
          </p>
        </div>
        <div class="grid md:grid-cols-3 gap-6">
          <div
            v-for="i in 3"
            :key="i"
            class="relative aspect-[3/4] rounded-2xl overflow-hidden bg-gray-100 dark:bg-gray-800 group"
          >
            <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent" />
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
        </div>
      </UContainer>
    </section>

    <!-- FAQ section -->
    <section
      id="faq"
      class="py-16 md:py-24 bg-white dark:bg-gray-950"
    >
      <UContainer>
        <div class="text-center max-w-3xl mx-auto mb-12">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Frequently asked questions
          </h2>
        </div>
        <UAccordion
          :items="faqItems"
          :ui="{ wrapper: 'space-y-2' }"
          class="max-w-3xl mx-auto"
        />
      </UContainer>
    </section>

    <!-- Social collage CTA -->
    <section class="py-16 md:py-24 bg-gray-50 dark:bg-gray-900/50">
      <UContainer>
        <div class="text-center mb-12">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
            Join us @SpaSupreme
          </h2>
          <p class="text-gray-600 dark:text-gray-400 text-lg mb-8">
            Share your wellness journey. Tag us for a chance to be featured.
          </p>
          <UButton
            to="#"
            target="_blank"
            color="primary"
            size="lg"
            class="rounded-full"
          >
            Follow on Instagram
          </UButton>
        </div>
        <div class="relative h-64 md:h-80 rounded-2xl overflow-hidden">
          <div class="absolute inset-0 flex items-center justify-center gap-4 p-4">
            <div
              v-for="(item, i) in 5"
              :key="i"
              class="w-24 h-32 md:w-32 md:h-40 rounded-xl bg-gray-200 dark:bg-gray-700 shadow-lg"
              :class="socialCollageRotations[i % 5]"
            />
          </div>
        </div>
      </UContainer>
    </section>
  </div>
</template>

<script setup lang="ts">
const products = [
  {
    id: 1,
    name: 'Energy',
    description: 'Sustained energy without the crash.',
    bgClass: 'bg-purple-100/50 dark:bg-purple-900/20',
    colorClass: 'bg-purple-400/70 dark:bg-purple-600/50'
  },
  {
    id: 2,
    name: 'Sleep',
    description: 'Restful nights, refreshed mornings.',
    bgClass: 'bg-primary-100/50 dark:bg-primary-900/20',
    colorClass: 'bg-primary-400/70 dark:bg-primary-600/50'
  },
  {
    id: 3,
    name: 'Focus',
    description: 'Sharp mind, clear thinking.',
    bgClass: 'bg-amber-100/50 dark:bg-amber-900/20',
    colorClass: 'bg-amber-600/60 dark:bg-amber-700/50'
  },
  {
    id: 4,
    name: 'Vitality',
    description: 'Whole-body wellness support.',
    bgClass: 'bg-secondary-100/50 dark:bg-secondary-900/20',
    colorClass: 'bg-secondary-400/70 dark:bg-secondary-600/50'
  }
]

const lifestyleBenefits = [
  'Ease of digestion',
  'No bloating',
  'No harsh chemicals',
  'No crash energy',
  'Cleaner formula'
]

const featureProducts = [
  {
    name: 'Daily Energy Complex',
    badge: 'Best Seller',
    description: 'A clinically studied blend of vitamins and adaptogens designed to support sustained energy throughout your day. No jitters, no crash—just steady, natural vitality.',
    chips: ['B vitamins', 'Ashwagandha', 'No caffeine crash'],
    bgClass: 'bg-primary-100/50 dark:bg-primary-900/30',
    colorClass: 'bg-primary-500/80 dark:bg-primary-600/60'
  },
  {
    name: 'Rest & Restore',
    badge: 'Natural',
    description: 'Promote deeper sleep with our melatonin-free formula. Magnesium, L-theanine, and calming botanicals help you wind down and wake up refreshed.',
    chips: ['Magnesium', 'L-theanine', 'Non-habit forming'],
    bgClass: 'bg-secondary-100/50 dark:bg-secondary-900/30',
    colorClass: 'bg-secondary-500/80 dark:bg-secondary-600/60'
  }
]

const socialCollageRotations = [
  'rotate-[-8deg] -translate-y-2',
  'rotate-[5deg] translate-y-4',
  'rotate-[-3deg]',
  'rotate-[7deg] -translate-y-1',
  'rotate-[-5deg] translate-y-2'
]

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
