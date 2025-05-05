<template>
  <nav class="flex items-center justify-between px-6 py-4">
    <ul class="flex gap-4">
      <Icon
        class="cursor-pointer"
        icon="akar-icons:shopping-bag"
        width="24"
        height="24"
      />
      <Icon
        class="cursor-pointer"
        icon="akar-icons:person"
        width="24"
        height="24"
      />
    </ul>
  </nav>
  <div>
    <div class="h-[80vh] bg-linear-65 from-sky-500 to-indigo-500"></div>
    <ul class="flex gap-6 pt-10 w-96">
      <li class="w-24 h-24">
        <img src="../public/wfactory.png" alt="Waffle Factory" />
      </li>
      <li class="w-24 h-24">
        <img src="../public/otacos.png" alt="O Tacos" />
      </li>
      <li class="w-24 h-24">
        <img src="../public/obrooklyn-2.png" alt="O Brooklyn" />
      </li>
      <li class="w-24 h-24">
        <img src="../public/planet-sushi.png" alt="Planet Sushi" />
      </li>
    </ul>
  </div>
</template>
