<script setup>
import { reactive, computed } from "vue";
import SectionHero from "./SectionHero.vue";
const { title } = defineProps(["title"]);
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. Props"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/Props.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      Title: {{ title }}
    </div>
  </div>
</template>
