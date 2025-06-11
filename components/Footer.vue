<template>
  <footer class="bg-[#F5F5F7] py-8 px-6">
    <img
      src="/logo-koliagram.svg"
      alt="Logo Koliagram (grand)"
      class="w-40 m-auto"
    />
    <nav
      class="flex flex-col gap-2 py-3 font-display text-center"
      aria-label="Navigation secondaire"
    >
      <p class="text-sm font-medium tracking-tight">En savoir plus</p>
      <NuxtLink to="/login" class="text-xs font-light">Se connecter</NuxtLink>
      <NuxtLink to="/register" class="text-xs font-light">S'inscrire</NuxtLink>
      <NuxtLink to="/" class="text-xs font-light">Réservez votre démo</NuxtLink>
      <p class="text-xs font-light pt-8 tracking-tight">
        Copyright &copy; {{ currentYear }} Koliagram. Tous droits réservés.
      </p>
    </nav>
  </footer>
</template>

<script lang="ts" setup>
const currentYear: number = new Date().getFullYear();
</script>
