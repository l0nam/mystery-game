<script setup>
import { ref } from "vue";
import { checkPassword } from "@/assets/js/qwerqwerty.js";

const inputPassword = ref("");
const message = ref("");

async function handleLogin() {
  const success = await checkPassword(inputPassword.value);
  if (!success) {
    message.value = "Wrong password!";
  }
}

useHead({
  title: "Password",
});
</script>

<template>
  <div class="container">
    <NuxtLink to="/" class="btn absolute top-[20px] left-[20px]">Back</NuxtLink>
    <h2 class="text-2xl font-bold">Enter Password</h2>

    <input v-model="inputPassword" type="password" placeholder="Password" />

    <button
      @click="handleLogin"
      class="btn"
    >
      OK
    </button>

    <p class="text-red-500">{{ message }}</p>
  </div>
</template>
