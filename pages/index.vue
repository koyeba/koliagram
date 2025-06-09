<template>
  <div class="px-6 sm:px-16 md:px-26 lg:px-36 xl:px-46 2xl:px-66">
    <div class="h-screen mb-16">
      <div
        class="flex flex-col gap-10 pt-35 lg:pt-50 text-center items-center mb-15 font-display"
      >
        <p class="text-sm bg-gray-100 rounded-4xl py-2 w-60">
          Bienvenue sur
          <NuxtLink to="/" class="font-bold text-[#FF630B]"
            >koliagram.com</NuxtLink
          >
        </p>
        <h1
          class="text-6xl lg:text-7xl xl:text-8xl 2xl:text-[6rem] font-bold tracking-tighter"
        >
          Maîtrisez <br class="lg:hidden" />
          votre image <br />
          en ligne <br class="lg:hidden" />à 100%
        </h1>
        <button
          type="button"
          class="px-10 py-4 rounded-full bg-[#FF630B] text-white font-semibold"
        >
          Réservez votre démo
        </button>
      </div>
      <div class="mb-12">
        <p class="text-center text-sm font-display">
          Les meilleurs établissement nous font
          <span class="font-bold"
            >confiance pour gérer leur présence en ligne.</span
          >
        </p>
      </div>
      <div
        class="flex gap-1 md:gap-10 justify-between md:justify-center mb-18 items-center"
      >
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
    <div class="mb-30">
      <h2 class="text-left text-4xl tracking-tighter font-display font-bold">
        Koliagram rend accessible sit amet consectetur, adipiscing elit.
        Phasellus a quam eu odio elementum venenatis.
      </h2>
    </div>
    <div class="h-screen mb-26">
      <div class="flex flex-col items-center text-center gap-10 font-display">
        <p class="text-sm bg-gray-100 rounded-3xl py-2 w-48 font-medium">
          Prise en main rapide
        </p>
        <h2 class="text-5xl font-bold tracking-tight">
          Votre image <br />
          est essentiel
        </h2>
        <p class="text-lg leading-7 tracking-tight font-light mb-15">
          <span
            >Répondre à ses avis clients ne devrait pas être une corvée.</span
          >
          On y réponds à votre place (ou non) avec vos directives.
        </p>
        <div
          class="w-full h-[30rem] bg-[url(/background-image-1.jpg)] bg-no-repeat bg-cover rounded-4xl shadow-2xl"
        ></div>
      </div>
    </div>
    <div class="flex flex-col items-center text-center gap-5 mb-20">
      <h2 class="text-center text-4xl tracking-tighter font-display font-bold">
        " Depuis qu'on a découvert Koliagram, on a jamais été aussi efficace sur
        nos retours clients négatifs "
      </h2>
      <p class="font-display tracking-tight font-semibold">
        - Gilles Robin, franchisé O'Tacos
      </p>
    </div>
    <div class="flex flex-col items-left text-center gap-10 mb-20">
      <p class="text-sm bg-gray-100 rounded-3xl py-2 w-36 font-medium">
        Animation
      </p>
      <h2 class="text-5xl font-bold tracking-tight text-left">
        Vos réseaux sociaux en pilote automatique
      </h2>
      <p class="text-left text-lg leading-7 tracking-tight font-light mb-15">
        <span>Répondre à ses avis clients ne devrait pas être une corvée.</span>
        On y réponds à votre place (ou non) avec vos directives.
      </p>
    </div>
    <div class="flex flex-col items-end gap-10 mb-20">
      <p
        class="text-sm text-center rounded-3xl py-2 w-42 font-medium bg-[#FF630B]"
      >
        Nos sur-mesures
      </p>
      <h2 class="text-5xl font-bold tracking-tight text-right">
        Création digitale <br />
        sur-mesure
      </h2>
      <div
        class="w-full h-96 bg-[url(/background-image-4.jpg)] bg-no-repeat bg-cover rounded-4xl shadow-2xl"
      ></div>
    </div>
  </div>
</template>
