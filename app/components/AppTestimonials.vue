<template>
  <div class="bg-dark-50 dark:bg-dark-950 relative h-auto w-full py-24">
    <div class="flex flex-col items-center justify-center gap-y-2">
      <!-- <UBadge color="primary" variant="soft"> Join the Movement </UBadge> -->
      <h1
        class="text-dark-950 dark:text-dark-50 text-center text-5xl font-light md:text-6xl"
      >
        Previous projects
      </h1>
      <p
        class="text-dark-950/50 dark:text-dark-50/50 mt-4 mx-auto w-full px-4 text-center md:w-1/2 md:p-0"
      >
        Discover my previous work in Tapau.
      </p>
    </div>
    <UContainer>
      <div class="mt-12 grid grid-cols-12 gap-4">
        <template v-for="(testimonial, index) in testimonials" :key="index">
          <div class="col-span-full grid grid-cols-2 gap-4 lg:col-span-6">
            <div class="col-span-full h-auto lg:col-span-1">
              <NuxtImg
                format="webp"
                :src="testimonial.img"
                class="h-96 w-full rounded-2xl object-cover object-center"
              />
            </div>
            <div
              class="bg-dark-100 dark:bg-dark-900/80 col-span-full flex flex-col items-start rounded-2xl p-4 lg:col-span-1 lg:items-center lg:justify-between"
            >
              <div class="flex w-full flex-col">
                <!-- <UIcon name="i-ri-double-quotes-r" class="size-8" /> -->
                <h2 class="text-dark-950 dark:text-dark-50 text-xl">
                  {{ testimonial.title }}
                </h2>
              </div>
              <div class="mt-12 flex flex-col">
                <p class="text-dark-950/60 dark:text-dark-50/60 text-base">
                  {{ testimonial.text }}
                </p>
                <span
                  class="text-dark-950/80 dark:text-dark-50/80 mt-1 text-base font-medium"
                >
                  {{ testimonial.name }}
                </span>
              </div>
            </div>
          </div>
        </template>
      </div>
    </UContainer>
  </div>
</template>

<script setup lang="ts">
const testimonials = shallowRef([
  {
    // name: "Emily Johnson",
    // username: "@emilyj",
    text: "This service transformed my business. The tools provided are easy to use and incredibly effective. Highly recommend!",
    title: "Building shed",
    img: "img/cabanon.jpeg",
  },
  {
    // name: "Ana Rodríguez",
    username: "@anarod",
    text: "Este servicio ha transformado mi negocio. Las herramientas son fáciles de usar y extremadamente efectivas. ¡Lo recomiendo mucho!",
    title: "Zinc roof",
    img: "img/zinc.jpeg",
  },
  //Add More data
]);
</script>
