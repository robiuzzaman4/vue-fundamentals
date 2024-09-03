<script setup>
import { inject } from "vue";

const data = inject("data");
</script>

<template>
  <p class="text-lg font-medium">{{ data.title }}</p>
  <p class="text-lg font-medium">{{ data.description }}</p>
</template>
