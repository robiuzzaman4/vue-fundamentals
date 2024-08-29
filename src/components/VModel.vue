<script setup>
import { ref } from "vue";
import SectionHero from "./SectionHero.vue";

const formData = ref({
  username: "",
  email: "",
});
</script>

<template>
  <div class="w-full grid gap-6">
    <SectionHero
      title="#. V-Model"
      github_url="https://github.com/robiuzzaman4/vue-fundamentals/blob/main/src/components/VModel.vue"
    />
    <div
      class="w-full bg-white border border-zinc-200 rounded-lg p-6 flex flex-col gap-6"
    >
      <div class="text-lg font-medium grid gap-1">
        <p>Username: {{ formData.username }}</p>
        <p>Email: {{ formData.email }}</p>
      </div>
      <form class="grid gap-2">
        <input
          v-model="formData.username"
          type="text"
          class="w-full px-3 py-1.5 rounded-lg focus-visible:outline-none border border-zinc-200 focus:border-zinc-950"
          placeholder="Enter your username"
        />
        <input
          v-model="formData.email"
          type="email"
          class="w-full px-3 py-1.5 rounded-lg focus-visible:outline-none border border-zinc-200 focus:border-zinc-950"
          placeholder="Enter your email"
        />
      </form>
    </div>
  </div>
</template>
