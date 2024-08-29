<script setup>
import { ref } from "vue";
import SectionHero from "./SectionHero.vue";

const fruits = ref(["Apple", "Mango", "Banana", "Lichi"]);

const handleAddNewFruit = () => {
  fruits.value.push("Avocado");
};

const handleRemove3rdItem = () => {
  fruits.value.splice(2, 1);
};
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="4. Ref"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/Ref.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <p class="text-sm font-medium">Fruits: {{ fruits }}</p>

      <div class="flex items-center gap-4">
        <button
          @click="handleAddNewFruit"
          class="h-9 px-3 py-1.5 rounded-lg bg-emerald-600 text-white text-sm font-medium w-fit"
        >
          Add 'Avocado'
        </button>
        <button
          @click="handleRemove3rdItem"
          class="h-9 px-3 py-1.5 rounded-lg bg-rose-600 text-white text-sm font-medium w-fit"
        >
          Remove 3rd Item
        </button>
      </div>
    </div>
  </div>
</template>
