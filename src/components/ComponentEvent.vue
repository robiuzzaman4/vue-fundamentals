<script setup>
import { ref } from "vue";
import SectionHero from "./SectionHero.vue";
import ComponentEventChild from "./ComponentEventChild.vue";

const count = ref(0);
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. Component Event"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/ComponentEvent.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <p class="text-lg font-medium">{{ count }}</p>
      <ComponentEventChild @increment="count++" @reset="count = 0" />
    </div>
  </div>
</template>
