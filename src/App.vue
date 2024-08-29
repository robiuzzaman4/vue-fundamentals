<script setup>
import ConditionalRendering from "./components/ConditionalRendering.vue";
import Reactive from "./components/Reactive.vue";
import ListRendering from "./components/ListRendering.vue";
import Ref from "./components/Ref.vue";
import ComputedProperties from "./components/ComputedProperties.vue";
import VFor from "./components/VFor.vue";
import VModel from "./components/VModel.vue";
import Props from "./components/Props.vue";
</script>

<template>
  <div class="w-full max-w-screen-md mx-auto px-6 py-12 grid gap-6">
    <ConditionalRendering />
    <ListRendering />
    <Ref />
    <Reactive />
    <ComputedProperties />
    <VFor />
    <VModel />
    <Props title="This title is passing form parent component" />
  </div>
</template>
