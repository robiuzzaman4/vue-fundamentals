<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  github_url: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="flex items-center justify-between gap-4">
    <h1 class="text-lg sm:text-xl font-medium">{{ title }}:</h1>
    <a :href="github_url" class="text-sm font-normal underline">Code</a>
  </div>
</template>
