<script setup>
import { ref } from "vue";
import SectionHero from "./SectionHero.vue";

const items = ref({
  framework_one: {
    name: "Next.js",
    website: "https://nextjs.org",
  },
  framework_two: {
    name: "Nuxt.js",
    website: "https://nuxt.com",
  },
});
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. V-For"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/VFor.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <!-- loop over root object -->
      <ul
        v-for="(item, keys, index) in items"
        :key="index"
        class="text-lg font-medium list-disc pl-1 sm:pl-4"
      >
        <li>
          {{ item }}
        </li>

        <!-- loop over nested object -->
        <li
          v-for="(property, keys, index) in item"
          key="index"
          class="flex items-center gap-1"
        >
          <p class="capitalize">{{ keys }}:</p>
          {{ property }}
        </li>
      </ul>
    </div>
  </div>
</template>
