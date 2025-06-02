<template>
  <div>
    <div class="py-4 px-6 sm:px-16 md:px-26 lg:px-36">
      <NuxtLink to="/"
        ><img
          src="../public/symbol-koliagram.svg"
          alt="koliagram"
          class="w-8 block md:hidden lg:hidden cursor-pointer" />
        <img
          src="../public/logo-koliagram.svg"
          alt="koliagram"
          class="w-40 hidden md:block lg:block cursor-pointer"
      /></NuxtLink>
    </div>
    <div
      class="flex items-center justify-center max-w-xl m-auto px-6 py-16 mt-35 md:shadow-sm rounded-xl font-display"
    >
      <div class="w-full px-6">
        <h1 class="text-center text-2xl font-bold mb-8">Se connecter</h1>
        <form @submit.prevent="handleLogin">
          <div class="mb-4">
            <label for="email" class="block text-sm mb-2 text-gray-600"
              >Email / Nom d'utilisateur
            </label>
            <input
              v-model="email"
              type="email"
              id="email"
              placeholder="helloworld@gmail.com"
              required
              class="mt-1 block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
            />
          </div>
          <div class="mb-8">
            <label for="password" class="block text-sm mb-2 text-gray-600"
              >Mot de passe</label
            >
            <input
              v-model="password"
              type="password"
              id="password"
              required
              class="mt-1 block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
            />
          </div>
          <button
            type="submit"
            class="w-full py-2 px-4 bg-[#FF630B] hover:bg-[#ff7223] text-white rounded-full cursor-pointer transition duration-200"
          >
            Se connecter
          </button>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
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
