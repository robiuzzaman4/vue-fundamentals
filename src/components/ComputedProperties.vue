<script setup>
import { reactive, computed } from "vue";
import SectionHero from "./SectionHero.vue";

const author = reactive({
  name: "John Doe",
  books: [
    "Vue 2 - Advanced Guide",
    "Vue 3 - Basic Guide",
    "Vue 4 - The Mystery",
  ],
});
// a computed ref
const publishedBooksMessage = computed(() => {
  return author.books.length > 0
    ? `Published books: ${author.books.length}`
    : "No books to publish";
});
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="2. Computed Properties"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/ComputedProperties.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <p class="text-lg font-medium">{{ publishedBooksMessage }}</p>
    </div>
  </div>
</template>
