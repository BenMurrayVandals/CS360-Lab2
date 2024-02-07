<template>
  <NuxtLink :to="path">
    <!-- BUTTON -->
    <button
      :class="[isActivePage ? 'bg-slate-700' : 'bg-slate-500 transition-colors duration-200 hover:bg-slate-500/[0.5]']"
      class="flex items-center justify-center px-4 py-2 rounded-lg"
    >
      <!-- TEXT -->
      <h3
        :class="[isActivePage ? 'font-bold underline underline-offset-4' : 'font-medium']"
        class="text-white text-base"
      >
        {{ data }}
      </h3>
    </button>
  </NuxtLink>
</template>

<script setup lang="ts">
defineProps<{
  data: string;
  isActivePage?: boolean;
  path: string;
}>();
</script>
