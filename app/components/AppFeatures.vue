<template>
  <div class="flex h-auto w-full flex-col gap-12 p-4 py-24 md:gap-24">
    <div class="flex flex-col items-center justify-center gap-y-4">
      <h1
        class="text-center text-4xl font-medium text-dark-950 lg:text-5xl dark:text-dark-50"
      >
        Transform Your Living Space with <br />
        Our Professional Building Services
      </h1>
      <p
        class="w-full text-center text-lg text-dark-950/50 lg:w-1/2 dark:text-dark-50/50"
      >
        From extensions and carports to new roofs and maintenance, our expert 
        services transform your living space, ensuring durability and style 
        that captivate and inspire.
      </p>
    </div>
    <div class="grid grid-cols-12 gap-y-16 md:gap-x-6">
      <template v-for="(feat, index) in features" :key="index">
        <div
          class="col-span-full flex h-auto flex-col items-start justify-between gap-x-4 gap-y-4 rounded-lg transition-all duration-300 ease-in-out md:col-span-6 lg:col-span-4 xl:flex-row"
        >
          <div
            class="flex h-12 w-12 flex-auto items-center justify-center rounded-xl border border-dark-950/20 bg-dark-950/5 xl:w-44 dark:border-dark-500/50 dark:bg-dark-50/10"
          >
            <UIcon
              :name="feat.icon"
              class="size-8 text-dark-950 dark:text-dark-50"
            />
          </div>
          <div class="flex w-auto flex-col gap-y-2">
            <span
              class="text-xl font-semibold text-dark-950 dark:text-dark-50"
              >{{ feat.title }}</span
            >
            <p
              class="text-base font-normal text-dark-950/50 dark:text-dark-50/50"
            >
              {{ feat.description }}
            </p>
          </div>
        </div>
      </template>
    </div>
  </div>
</template>

<script setup lang="ts">
const features = [
  {
    icon: "i-heroicons-home-modern",
    title: "Extension Construction",
    description:
      "Expand your living space with our expertly designed and built home extensions. We handle everything from planning to completion.",
    link: "#",
  },
  {
    icon: "i-heroicons-truck",
    title: "Carport Installation",
    description:
      "Protect your vehicles with a durable, custom-built carport. Our designs blend functionality and style to complement your home.",
    link: "#",
  },
  {
    icon: "i-heroicons-wrench-screwdriver-16-solid",
    title: "Small Renovations",
    description:
      "Transform your space with our professional renovation services. From kitchen upgrades to bathroom remodels, we ensure quality craftsmanship.",
    link: "#",
  },
  {
    icon: "i-heroicons-cloud",
    title: "Shed Building",
    description:
      "Add practical storage or workspace with our custom-built sheds. We offer various sizes and styles to fit your needs and property.",
    link: "#",
  },
  {
    icon: "i-heroicons-home-solid",
    title: "New Roof Installation",
    description:
      "Enhance your home's value and protection with a new roof. Our team uses top-quality materials for durable, long-lasting results.",
    link: "#",
  },
  {
    icon: "i-heroicons-cog-6-tooth-20-solid",
    title: "Roof Maintenance",
    description:
      "Keep your roof in top condition with our maintenance services. We handle leak repairs, barge, and fascia metal cover replacements to extend your roof's lifespan.",
    link: "#",
  },
];
</script>
