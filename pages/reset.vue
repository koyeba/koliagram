<template>
  <div>
    <nav
      class="w-full fixed top-0 z-50 bg-white"
      aria-label="Navigation principale"
    >
      <div
        class="max-w-[100rem] mx-auto py-4 px-6 sm:px-8 md:px-12 lg:px-16 xl:px-20 2xl:px-24 transition-padding duration-300"
      >
        <!-- Logo -->
        <NuxtLink to="/" aria-label="Accueil">
          <img
            src="/symbol-koliagram.svg"
            alt="Logo Koliagram (petit)"
            class="w-8 block md:hidden"
          />
          <img
            src="/logo-koliagram.svg"
            alt="Logo Koliagram (grand)"
            class="w-40 hidden md:block"
          />
        </NuxtLink>
      </div>
    </nav>
    <div
      class="font-display mt-20 py-12 max-w-lg m-auto px-12 rounded-2xl lg:shadow-md"
    >
      <h1 class="text-2xl font-bold mb-14 text-center">
        Réinitialisation du mot de passe
      </h1>
      <form class="flex flex-col text-sm">
        <div class="mb-6">
          <label for="email" class="block text-sm mb-2 text-gray-600"
            >Email</label
          >
          <input
            type="email"
            id="email"
            placeholder="helloworld@gmail.com"
            required
            class="mt-1 block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
          />
        </div>
        <button
          type="submit"
          class="w-full py-2 px-4 bg-[#FF630B] hover:bg-[#ff7223] text-white rounded-full cursor-pointer transition duration-200"
        >
          Continuer
        </button>
      </form>
      <div>
        <p class="text-center text-xs text-gray-600 mt-4">
          <NuxtLink to="/login" class="text-[#FF630B] hover:text-black"
            >Revenir à la page de connexion</NuxtLink
          >
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
definePageMeta({
  layout: "auth",
});
</script>
