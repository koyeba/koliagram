<template>
  <div class="h-screen">
    <div
      class="flex flex-col gap-10 pt-35 text-center items-center mb-20 font-display"
    >
      <p class="text-sm bg-gray-100 rounded-2xl py-2 w-64">
        Bienvenue sur
        <NuxtLink to="/" class="font-bold text-[#FF630B]"
          >koliagram.com</NuxtLink
        >
      </p>
      <h1 class="text-6xl font-bold px-6 tracking-tighter">
        Maîtrisez <br />
        votre image <br />
        en ligne <br />à 100%
      </h1>
      <button
        type="button"
        class="px-10 py-4 rounded-full bg-[#FF630B] text-white font-semibold"
      >
        Réservez votre démo
      </button>
    </div>
    <div class="px-6 mb-6">
      <p class="text-center text-sm font-display">
        Les meilleurs établissement nous font
        <span class="font-bold"
          >confiance pour gérer leur présence en ligne.</span
        >
      </p>
    </div>
    <div class="flex gap-1 justify-between px-6 mb-18 items-center">
      <img src="/logo-otacos.png" alt="Logo O'Tacos" class="w-18" />
      <img
        src="/logo-wafflefactory.png"
        alt="Logo Waffle Factory"
        class="h-6"
      />
      <img src="/logo-obrooklyn.png" alt="Logo O'Brooklyn" class="w-16" />
      <img src="/logo-planetsushi.png" alt="Logo Planet Sushi" class="w-20" />
    </div>
  </div>
</template>
