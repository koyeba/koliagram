<template>
  <div>
    <div class="py-6 px-6 sm:px-16 md:px-26 lg:px-36 xl:px-46">
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
    <div
      class="font-display mt-16 py-12 max-w-lg m-auto px-12 rounded-2xl lg:shadow-md"
    >
      <h1 class="text-2xl font-bold mb-14 text-center">S'inscrire</h1>
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
            class="block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
          />
        </div>
        <div class="mb-6">
          <label for="username" class="block text-sm mb-2 text-gray-600"
            >Nom d'utilisateur / établissement</label
          >
          <input
            type="text"
            placeholder="mcdonaldschampselysee"
            class="block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
          />
        </div>
        <div class="mb-6">
          <label for="password" class="block text-sm mb-2 text-gray-600"
            >Mot de passe</label
          >
          <input
            type="password"
            required
            placeholder="Mot de passe"
            class="block w-full text-sm px-4 py-2 border border-gray-200 rounded-full focus:outline-none focus:ring-1 focus:ring-[#FF630B]"
          />
        </div>
        <button
          type="submit"
          class="w-full py-2 px-4 bg-[#FF630B] hover:bg-[#ff7223] text-white rounded-full cursor-pointer transition duration-200"
        >
          S'inscrire
        </button>
      </form>
      <div>
        <p class="text-center text-xs text-gray-600 mt-4">
          Vous avez déjà un compte ?
          <NuxtLink to="/login" class="text-[#FF630B] hover:text-black"
            >Connectez-vous</NuxtLink
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
