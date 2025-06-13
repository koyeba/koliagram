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
    <h2 id="register-title" class="sr-only">Inscription à Koliagram</h2>
    <form
      role="form"
      class="text-sm flex flex-col w-full gap-1"
      aria-labelledby="register-title"
    >
      <label for="email" class="block text-gray-600"
        >Email / Nom d'utilisateur
      </label>
      <input
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
        autocomplete="current-password"
        type="password"
        id="password"
        placeholder="Mot de passe"
        required
        aria-required="true"
        class="px-4 py-2 border border-gray-200 focus:outline-none focus:ring-1 focus:ring-[#FF630B] focus-visible:ring-offset-2 rounded-full"
      />
      <button
        type="submit"
        class="w-full mt-4 py-2 px-4 bg-[#FF630B] hover:bg-[#ff7223] text-white rounded-full cursor-pointer transition duration-200"
        aria-label="S'inscrire à votre Koliagram"
      >
        S'inscrire
      </button>
      <p class="text-center text-xs text-gray-600 mt-2">
        Vous avez déjà un compte ?
        <NuxtLink to="/login" class="text-[#FF630B] hover:text-black"
          >Connectez-vous</NuxtLink
        >
      </p>
    </form>
  </div>
</template>

<script lang="ts" setup>
definePageMeta({
  layout: "auth",
});
</script>
