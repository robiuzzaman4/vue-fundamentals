<script setup>
import { ref, computed } from "vue";
import SectionHero from "./SectionHero.vue";
</script>

<template>
  <div class="w-full grid gap-6">
    <div class="flex items-center gap-2">
      <button
        @click="$emit('increment')"
        class="h-9 px-3 py-1.5 rounded-lg bg-emerald-600 text-white text-sm font-medium w-fit"
      >
        Increment
      </button>
      <button
        @click="$emit('reset')"
        class="h-9 px-3 py-1.5 rounded-lg bg-zinc-600 text-white text-sm font-medium w-fit"
      >
        Reset
      </button>
    </div>
  </div>
</template>
