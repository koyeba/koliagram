<template>
  <nav
    class="w-full fixed py-4 px-6 sm:px-16 md:px-26 lg:px-36 xl:px-46"
    aria-label="Navigation principale"
  >
    <div class="flex justify-between">
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
      <div class="flex items-center gap-2">
        <NuxtLink
          to="/login"
          aria-label="Connexion"
          class="text-white text-xs font-display px-3 py-2 rounded-full bg-[#FF630B] hover:bg-[#ff7223]"
        >
          Se connecter
        </NuxtLink>
        <div
          class="text-black hover:bg-black hover:text-white text-xs font-display px-3 py-2 rounded-full border"
          aria-label="Réservez votre démo"
        >
          Réservez votre démo
        </div>
      </div>
    </div>
  </nav>
</template>
