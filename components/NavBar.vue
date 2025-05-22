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
      <div class="flex gap-3 md:gap-4 lg:gap-6 xl:gap-6 items-center">
        <button
          class="font-display text-xs cursor-pointer rounded-full bg-[#FF630B] hover:bg-[#ff7223] px-3 py-2 text-white"
        >
          Se connecter
        </button>
        <div class="lg:hidden">
          <button @click="toggleMenu">
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
                      dur="0.2s"
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
                      dur="0.2s"
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
                      dur="0.2s"
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
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const isOpen = ref(false);

function toggleMenu() {
  isOpen.value = !isOpen.value;
}
</script>
