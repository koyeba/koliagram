<template>
  <div>
    <div class="py-4 px-6 sm:px-16 md:px-26 lg:px-36 xl:px-46">
      <NuxtLink to="/" aria-label="Accueil">
        <!-- Logo Mobile -->
        <img
          src="/symbol-koliagram.svg"
          alt="Logo Koliagram (petit)"
          class="w-8 block md:hidden"
        />
        <!-- Logo Desktop -->
        <img
          src="/logo-koliagram.svg"
          alt="Logo Koliagram (grand)"
          class="w-40 hidden md:block"
        />
      </NuxtLink>
    </div>
    <div class="flex max-w-lg m-auto mt-20 py-12 rounded-2xl lg:shadow-md">
      <div class="font-display w-full px-12">
        <h1 class="text-center text-2xl font-bold mb-14">Se connecter</h1>
        <form @submit.prevent="handleLogin">
          <div class="mb-6">
            <label for="email" class="block text-sm mb-2 text-gray-600"
              >Email / Nom d'utilisateur
            </label>
            <input
              v-model="email"
              type="email"
              id="email"
              placeholder="helloworld@gmail.com"
              required
              class="block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
            />
          </div>
          <div class="mb-6">
            <label for="password" class="block text-sm mb-2 text-gray-600"
              >Mot de passe</label
            >
            <input
              v-model="password"
              type="password"
              id="password"
              placeholder="Mot de passe"
              required
              class="block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
            />
            <div class="text-right">
              <NuxtLink
                to="/reset"
                class="text-xs text-gray-400 hover:text-gray-200"
              >
                Mot de passe oublié ?
              </NuxtLink>
            </div>
          </div>
          <button
            type="submit"
            class="w-full py-2 px-4 bg-[#FF630B] hover:bg-[#ff7223] text-white rounded-full cursor-pointer transition duration-200"
          >
            Se connecter
          </button>
        </form>
        <div>
          <p class="text-center text-xs text-gray-600 mt-4">
            Vous n'avez pas de compte ?
            <NuxtLink to="/register" class="text-[#FF630B] hover:text-black"
              >Inscrivez-vous</NuxtLink
            >
          </p>
        </div>
      </div>
    </div>
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
