<script setup>
import { ref } from "vue";
import { checkDiscordID } from "@/assets/js/discord.js";

const discordID = ref("");
const message = ref("");

async function validate() {
  message.value = await checkDiscordID(discordID.value);
}

useHead({
  title: "Discord",
});
</script>

<template>
  <div class="container">
    <NuxtLink to="/" class="btn absolute top-[20px] left-[20px]">Back</NuxtLink>
    <h2 class="text-2xl font-bold">Discord</h2>
    <input
      v-model="discordID"
      type="text"
      placeholder="discord"
    />
    <button
      @click="validate"
      class="btn"
    >
      OK
    </button>
    <p v-if="message" class="text-white/60">{{ message }}</p>
  </div>
</template>
