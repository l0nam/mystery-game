<script setup>
import { useHead } from "#imports";
import '@/assets/js/index.js'

useHead({
  title: "Enter the Void",
});
</script>

<template>
  <div class="container">
    <div
      class="absolute min-h-[100svh] min-w-full z-[-1] top-0 left-0 opacity-30"
      style="
        background-image: url('./darkpass.png');
        background-repeat: no-repeat;
        background-size: cover;
      "
    ></div>
    <h1 class="text-3xl font-bold">Darkness surrounds you...</h1>
    <p class="text-lg text-gray-400">Follow the whispers.</p>
    <!-- 1e7cf18d5b89746df3b90b0f8fffae56 -->

    <NuxtLink to="/mystery" class="btn"> Record №014 </NuxtLink>
  </div>
</template>
