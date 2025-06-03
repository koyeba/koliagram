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
      <p class="text-sm">En savoir plus</p>
      <NuxtLink to="/login" class="text-xs font-thin">Se connecter</NuxtLink>
      <p class="text-xs font-thin cursor-pointer">Réservez votre démo</p>
      <p class="text-xs font-thin pt-8">
        Copyright &copy; {{ currentYear }} Koliagram. Tous droits réservés.
      </p>
    </nav>
  </footer>
</template>

<script lang="ts" setup>
const currentYear: number = new Date().getFullYear();
</script>
