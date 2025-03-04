<template>
    <footer class="relative flex h-auto max-h-dvh w-full flex-col gap-y-56 p-4">
      <div
        class="border-dark-950/5 dark:border-dark-50/5 grid w-full grid-cols-12 gap-6 border-t pt-12"
      >
        <div class="col-span-6 flex items-start justify-start lg:col-span-6">
          <span class="text-dark-950 dark:text-dark-50 text-2xl uppercase"
            >Let's Connect</span
          >
        </div>
        <template v-for="(nav, index) in address_company" :key="index">
          <div class="col-span-6 flex w-full flex-col gap-y-2 lg:col-span-2">
            <span
              class="text-dark-950 dark:text-dark-50 font-inter inline-block text-2xl uppercase"
            >
              {{ nav.label }}
            </span>
            <p
              class="text-dark-950/60 dark:text-dark-50/60 font-inter inline-block text-sm"
            >
              {{ nav.address }}
            </p>
            <span
              class="text-dark-950/60 dark:text-dark-50/60 font-inter inline-block text-sm"
            >
              {{ nav.email }}
            </span>
            <span
              class="text-dark-950/60 dark:text-dark-50/60 font-inter inline-block text-sm"
            >
              {{ nav.phone }}
            </span>
          </div>
        </template>
      </div>
    </footer>
  </template>
  
  <script setup lang="ts">
  
  const address_company = [
    {
      label: "New Zeland",
      address:
        "65 Taupo view road 3330 Taupo",
      phone: "0275267152",
      email: "xxx@company.com",
    }
  ];

  </script>