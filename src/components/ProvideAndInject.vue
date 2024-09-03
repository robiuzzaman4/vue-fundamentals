<script setup>
import { provide } from "vue";
import SectionHero from "./SectionHero.vue";
import SchoolComponent from "./SchoolComponent.vue";

provide("data", {
  title: "Provide and Inject Example:",
  description:
    "This student data is passed to the nested components without using props.",
});
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. Provide and Inject"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/ProvideAndInject.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <SchoolComponent />
    </div>
  </div>
</template>
