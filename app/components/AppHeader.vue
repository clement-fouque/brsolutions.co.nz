<script setup lang="ts">
const items = ref([
  {
    label: "Home",
    icon: "material-symbols:home-app-logo",
    to: "#",
  },
  {
    label: "Services",
    // icon: 'i-lucide-database',
    to: "#",
  },
  {
    label: "Contact",
    // icon: 'i-simple-icons-github',
    // badge: '3.8k',
    to: "#",
  },
]);
</script>

<template>
  <UNavigationMenu :items="items" class="w-full justify-center" />
</template>
