<template>
  <footer
    class="bg-[#F5F5F7] py-8 px-6 sm:px-16 md:px-26 lg:px-36 font-display xl:text-center"
  >
    <img
      src="../public/logo-koliagram.svg"
      alt="Logo koliagram"
      class="w-36 pb-2 xl:m-auto"
    />
    <div class="py-3 flex flex-col gap-2">
      <p class="text-sm cursor-pointer">En savoir plus</p>
      <p class="text-xs font-thin cursor-pointer">Sentinelle</p>
      <p class="text-xs font-thin cursor-pointer">Créations</p>
      <p class="text-xs font-thin cursor-pointer">Réseaux sociaux</p>
      <p class="text-xs font-thin cursor-pointer">
        Contacter notre support 24/7
      </p>
      <p class="text-xs pt-10 font-thin cursor-pointer">Mentions Légales</p>
      <p class="text-xs font-thin cursor-pointer">
        Politique de confidentialité
      </p>
      <p class="text-xs font-thin cursor-pointer">Utilisation des cookies</p>
      <p class="text-xs pt-5 font-thin">
        Copyright &copy; {{ new Date().getFullYear() }} Koliagram. Tous droits
        réservés.
      </p>
    </div>
  </footer>
</template>
