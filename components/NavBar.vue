<template>
  <nav class="w-full fixed py-4 px-6 sm:px-16 md:px-26 lg:px-36">
    <div class="flex justify-between">
      <NuxtLink to="/"
        ><img
          src="../public/symbol-koliagram.svg"
          alt="koliagram"
          class="w-8 block md:hidden lg:hidden cursor-pointer" />
        <img
          src="../public/logo-koliagram.svg"
          alt="koliagram"
          class="w-40 hidden md:block lg:block cursor-pointer"
      /></NuxtLink>
      <div class="flex gap-6 md:gap-4 lg:gap-6 xl:gap-6 items-center">
        <NuxtLink
          to="/login"
          class="font-display text-xs cursor-pointer rounded-full bg-[#FF630B] hover:bg-[#ff7223] px-3 py-2 text-white"
        >
          Se connecter
        </NuxtLink>
        <div class="lg:hidden">
          <button
            @click="toggleMenu"
            class="fixed top-3 right-4 z-50 mt-1 focus:outline-none"
          >
            <template v-if="!isOpen">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                class="mt-1"
              >
                <g
                  fill="none"
                  stroke="#000"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                >
                  <path d="M5 5L19 19M5 19L19 5">
                    <animate
                      fill="freeze"
                      attributeName="d"
                      dur="0.4s"
                      values="M5 5L19 19M5 19L19 5;M5 5L19 5M5 19L19 19"
                    />
                  </path>
                  <path d="M12 12H12" opacity="0">
                    <animate
                      fill="freeze"
                      attributeName="d"
                      begin="0.2s"
                      dur="0.2s"
                      values="M12 12H12;M5 12H19"
                    />
                    <set
                      fill="freeze"
                      attributeName="opacity"
                      begin="0.2s"
                      to="1"
                    />
                  </path>
                </g>
              </svg>
            </template>
            <template v-else>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                class="mt-1"
              >
                <g
                  fill="none"
                  stroke="#000"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                >
                  <path d="M5 12H19">
                    <animate
                      fill="freeze"
                      attributeName="d"
                      dur="0.1s"
                      values="M5 12H19;M12 12H12"
                    />
                    <set
                      fill="freeze"
                      attributeName="opacity"
                      begin="0.4s"
                      to="0"
                    />
                  </path>
                  <path d="M5 5L19 5M5 19L19 19" opacity="0">
                    <animate
                      fill="freeze"
                      attributeName="d"
                      begin="0.2s"
                      dur="0.1s"
                      values="M5 5L19 5M5 19L19 19;M5 5L19 19M5 19L19 5"
                    />
                    <set
                      fill="freeze"
                      attributeName="opacity"
                      begin="0s"
                      to="1"
                    />
                  </path>
                </g>
              </svg>
            </template>
          </button>
          <transition name="slide-down">
            <nav
              v-if="isOpen"
              class="fixed top-0 left-0 px-6 py-14 w-full h-full bg-white text-black font-display z-40 flex flex-col items-end text-right"
            >
              <ul class="space-y-4 font-thin">
                <li>
                  <a href="#" class="text-sm">Réserver votre démo</a>
                </li>
              </ul>
            </nav>
          </transition>
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts" setup>
import { ref, watch } from "vue";

const isOpen = ref(false);

function toggleMenu() {
  isOpen.value = !isOpen.value;
}

watch(isOpen, (newVal) => {
  if (newVal) {
    document.body.style.overflow = "hidden";
  } else {
    document.body.style.overflow = "";
  }
});
</script>

<style scoped>
.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.5s ease-in-out;
}
.slide-down-enter-from {
  transform: translateY(-100%);
}
.slide-down-enter-to {
  transform: translateY(0);
}
.slide-down-leave-from {
  transform: translateY(0);
}
.slide-down-leave-to {
  transform: translateY(-100%);
}
</style>
