<script setup>
import { ref, computed } from "vue";
import SectionHero from "./SectionHero.vue";
const number = ref(4);
const squearedNumber = computed(() => {
  return number.value * number.value;
});

const increamentNumber = () => {
    number.value++;
  };

</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. Computed Properties"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/ComputedProperties.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <p class="text-lg font-medium">Number: {{ number }}</p>
      <p class="text-lg font-medium">Squared Number: {{ squearedNumber }}</p>
      <button
          @click="increamentNumber"
          class="h-9 px-3 py-1.5 rounded-lg bg-emerald-600 text-white text-sm font-medium w-fit"
        >
          Increament Number
        </button>
    </div>
  </div>
</template>
