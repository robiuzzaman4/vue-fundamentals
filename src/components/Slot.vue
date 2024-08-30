<script setup>
import SectionHero from "./SectionHero.vue";
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. Slot"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/Slot.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <slot name="slot_one"></slot>
      <slot name="slot_two"></slot>
    </div>
  </div>
</template>
