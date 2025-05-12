<template>
  <nav class="w-full fixed px-6 sm:px-16 md:px-26 lg:px-36 py-4">
    <div class="flex justify-between">
      <img
        src="../public/symbol-koliagram.svg"
        alt="koliagram"
        class="w-8 block md:hidden lg:hidden cursor-pointer"
      />
      <img
        src="../public/logo-koliagram.svg"
        alt="koliagram"
        class="w-40 hidden md:block lg:block cursor-pointer"
      />
      <div class="flex gap-4 md:gap-4 lg:gap-6 xl:gap-6 items-center">
        <button
          class="font-display text-sm mt-1 cursor-pointer rounded-full bg-[#FF630B] hover:bg-[#ff7223] px-3 py-2 text-white"
        >
          Se connecter
        </button>
        <Icon
          class="cursor-pointer"
          icon="weui:shop-outlined"
          width="24"
          height="24"
        />
        <Icon
          icon="iconamoon:menu-burger-horizontal-thin"
          width="24"
          height="24"
          class="mt-1 lg:hidden"
        />
        <button
          class="hidden pr-3 py-2 lg:block text-sm mt-1 font-display cursor-pointer hover:text-[#FF630B]"
        >
          Réservez votre démo
        </button>
      </div>
    </div>
  </nav>
</template>
