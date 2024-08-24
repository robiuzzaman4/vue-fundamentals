<script setup>
import { ref } from "vue";
import SectionHero from "./SectionHero.vue";

const isVueAwesome = ref(true);

const handleToggle = () => {
  isVueAwesome.value = !isVueAwesome.value;
};
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="1. Conditional Rendering"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/ConditionalRendering.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 grid gap-6"
    >
      <button
        @click="handleToggle"
        class="h-9 px-3 py-1.5 rounded-lg bg-emerald-600 text-white text-sm font-medium w-fit"
      >
        Toggle
      </button>

      <!-- render and style with conditionally -->
      <h3 v-if="isVueAwesome" class="text-3xl font-medium">Vue is awesome</h3>
      <h3
        v-else
        class="text-3xl font-medium"
        :class="{ 'text-red-500': !isVueAwesome }"
      >
        Oh no 😪
      </h3>
    </div>
  </div>
</template>
