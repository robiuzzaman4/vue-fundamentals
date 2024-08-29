<script setup>
import ConditionalRendering from "./components/ConditionalRendering.vue";
import ComputedProperties from "./components/ComputedProperties.vue";
import ListRendering from "./components/ListRendering.vue";
import Ref from "./components/Ref.vue";
</script>

<template>
  <div class="w-full max-w-screen-md mx-auto px-6 py-12 grid gap-6">
    <ConditionalRendering />
    <ComputedProperties />
    <ListRendering />
    <Ref />
  </div>
</template>
