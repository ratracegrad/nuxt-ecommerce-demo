<template>
  <UPageSection
    id="science"
    title="Why SpaSupreme?"
    description="We combine clinical-grade ingredients with natural wellness to deliver results you can feel."
    orientation="vertical"
  >
    <template #body>
      <UPageGrid>
        <UPageCard
          variant="outline"
          class="rounded-xl shadow-lg"
        >
          <template #header>
            <div class="flex items-start gap-4">
              <div class="p-2 rounded-lg bg-secondary-100">
                <UIcon
                  name="i-lucide-leaf"
                  class="size-9 text-secondary-600"
                />
              </div>
              <div>
                <UBadge
                  color="secondary"
                  variant="soft"
                  class="rounded-full mb-2"
                >
                  Natural
                </UBadge>
                <h3 class="font-semibold text-lg">
                  Clean Ingredients
                </h3>
              </div>
            </div>
          </template>
          <template #body>
            <p>
              No artificial fillers, no harsh chemicals. Every ingredient is selected for purity and efficacy.
            </p>
          </template>
        </UPageCard>
        <UPageCard
          variant="outline"
          class="rounded-xl shadow-lg"
        >
          <template #header>
            <div class="flex items-start gap-4">
              <div class="p-2 rounded-lg bg-primary-100">
                <UIcon
                  name="i-lucide-flask-conical"
                  class="size-9 text-primary-600"
                />
              </div>
              <div>
                <UBadge
                  color="primary"
                  variant="soft"
                  class="rounded-full mb-2"
                >
                  Proven
                </UBadge>
                <h3 class="font-semibold text-lg">
                  Science-Backed
                </h3>
              </div>
            </div>
          </template>
          <template #body>
            <p>
              Formulated with clinically studied doses. We prioritize what works, not what sells.
            </p>
          </template>
        </UPageCard>
        <UPageCard
          variant="outline"
          class="rounded-xl shadow-lg"
        >
          <template #header>
            <div class="flex items-start gap-4">
              <div class="p-2 rounded-lg bg-secondary-100">
                <UIcon
                  name="i-lucide-heart"
                  class="size-9 text-secondary-600"
                />
              </div>
              <div>
                <UBadge
                  color="secondary"
                  variant="soft"
                  class="rounded-full mb-2"
                >
                  Gentle
                </UBadge>
                <h3 class="font-semibold text-lg">
                  Easy on Your Body
                </h3>
              </div>
            </div>
          </template>
          <template #body>
            <p>
              No bloating, no crash. Our formulas are designed for daily use without harsh side effects.
            </p>
          </template>
        </UPageCard>
      </UPageGrid>
    </template>
  </UPageSection>
</template>
