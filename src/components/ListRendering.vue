<script setup>
import { ref } from "vue";
import SectionTitle from "./SectionTitle.vue";

const items = ref([
  { framework: "Next.js" },
  { framework: "Nuxt.js" },
  { framework: "Nest.js" },
]);
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionTitle title="List Rendering" />
    <div
      class="w-full max-w-96 bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <h3 class="text-sm font-medium">Frameworks:</h3>
      <!-- render list items -->
      <ul
        class="list-disc text-zinc-500 pl-4"
        v-for="(item, index) in items"
        :key="index"
      >
        <li class="text-sm -my-2">
          {{ item.framework }}
        </li>
      </ul>
    </div>
  </div>
</template>
