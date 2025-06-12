<template>
  <footer class="bg-gray-100 py-8 px-6 mt-6">
    <img src="/logo-koliagram.svg" alt="Logo Koliagram (grand)" class="w-40" />
    <nav
      class="flex flex-col gap-2 py-3 font-display text-left text-sm"
      aria-label="Navigation secondaire"
    >
      <NuxtLink to="/login">Se connecter</NuxtLink>
      <NuxtLink to="/" class="mb-8">Réservez votre démo</NuxtLink>
      <p class="tracking-tight">
        Copyright &copy; {{ currentYear }} Koliagram. Tous droits réservés.
      </p>
    </nav>
  </footer>
</template>

<script lang="ts" setup>
const currentYear: number = new Date().getFullYear();
</script>
