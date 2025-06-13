<template>
  <div
    class="h-lvh flex flex-col justify-center items-center px-6 gap-10 md:gap-20 md:max-w-lg md:m-auto"
  >
    <NuxtLink to="/">
      <img
        src="/logo-koliagram.svg"
        alt="Logo Koliagram (grand)"
        class="w-40 md:w-60"
    /></NuxtLink>
    <h2 id="login-title" class="sr-only">Connexion à Koliagram</h2>
    <form
      role="form"
      @submit.prevent="handleLogin"
      class="text-sm flex flex-col w-full gap-1"
      aria-labelledby="login-title"
    >
      <label for="email" class="block text-gray-600"
        >Email / Nom d'utilisateur
      </label>
      <input
        v-model="email"
        autocomplete="username"
        type="email"
        id="email"
        placeholder="helloworld@gmail.com"
        required
        aria-required="true"
        class="px-4 py-2 border border-gray-200 focus:outline-none focus:ring-1 focus:ring-[#FF630B] focus-visible:ring-offset-2 rounded-full mb-4"
      />
      <label for="password" class="block text-gray-600">Mot de passe</label>
      <input
        v-model="password"
        autocomplete="current-password"
        type="password"
        id="password"
        placeholder="Mot de passe"
        required
        aria-required="true"
        class="px-4 py-2 border border-gray-200 focus:outline-none focus:ring-1 focus:ring-[#FF630B] focus-visible:ring-offset-2 rounded-full"
      />
      <div class="text-right">
        <NuxtLink to="/reset" class="text-xs text-gray-400 hover:text-gray-200">
          Mot de passe oublié ?
        </NuxtLink>
      </div>
      <button
        type="submit"
        class="w-full mt-4 py-2 px-4 bg-[#FF630B] hover:bg-[#ff7223] text-white rounded-full cursor-pointer transition duration-200"
        aria-label="Se connecter à votre compte"
      >
        Se connecter
      </button>
      <p class="text-center text-xs text-gray-600 mt-2">
        Vous n'avez pas de compte ?
        <NuxtLink to="/register" class="text-[#FF630B] hover:text-black"
          >Inscrivez-vous</NuxtLink
        >
      </p>
    </form>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

definePageMeta({
  layout: "auth",
});

const email = ref("");
const password = ref("");

const handleLogin = () => {
  console.log("Connexion avec :", email.value, password.value);
};
</script>
