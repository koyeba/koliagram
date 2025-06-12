<template>
  <nav class="w-full fixed top-0 z-50" aria-label="Navigation principale">
    <div
      class="bg-white mx-auto flex justify-between items-center py-2 px-6 sm:px-8 md:px-12 lg:px-16 xl:px-20 2xl:px-24 transition-padding duration-30"
    >
      <!-- Logo -->
      <NuxtLink to="/" aria-label="Accueil" class="flex items-center">
        <img
          src="/symbol-koliagram.svg"
          alt="Logo Koliagram (petit)"
          class="w-8 block md:hidden"
        />
        <img
          src="/logo-koliagram.svg"
          alt="Logo Koliagram (grand)"
          class="w-40 hidden md:block"
        />
      </NuxtLink>

      <!-- Desktop menu -->
      <div
        class="flex items-center gap-4 text-sm font-display font-medium py-1 md:pr-1"
      >
        <NuxtLink
          to="/login"
          aria-label="Connexion"
          class="bg-[#FF630B] hover:bg-[#CC5009] px-5 py-2 text-white rounded-full transition-colors duration-300"
        >
          Se connecter
        </NuxtLink>
        <NuxtLink
          to="/"
          aria-label="Réservez votre démo"
          class="hidden md:block hover:bg-gray-100 px-4 py-2 rounded-full transition-colors duration-300 text-[#333336] hover:text-black"
        >
          Réservez votre démo
        </NuxtLink>

        <!-- Mobile menu button -->
        <button
          @click="isMobileMenuOpen = !isMobileMenuOpen"
          class="md:hidden flex items-center justify-center z-100 cursor-pointer"
          aria-label="Menu mobile"
          :aria-expanded="isMobileMenuOpen"
        >
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1.2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <line
              x1="3"
              y1="7"
              x2="19"
              y2="7"
              :class="{ 'transform-top': isMobileMenuOpen }"
            />
            <line
              x1="3"
              y1="17"
              x2="19"
              y2="17"
              :class="{ 'transform-bottom': isMobileMenuOpen }"
            />
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile menu -->
    <transition name="slide-down">
      <nav
        v-if="isMobileMenuOpen"
        class="md:hidden fixed inset-0 h-screen z-60 px-12 overflow-hidden flex flex-col items-start gap-4 bg-white pt-14 text-xl font-display font-medium tracking-tight text-[#333336]"
        aria-label="Navigation mobile"
      >
        <NuxtLink
          to="/login"
          @click="isMobileMenuOpen = false"
          aria-label="Connexion"
          class="hover:text-black"
        >
          Se connecter
        </NuxtLink>
        <NuxtLink
          to="/"
          @click="isMobileMenuOpen = false"
          aria-label="Réservez votre démo"
          class="hover:text-black"
        >
          Réservez votre démo
        </NuxtLink>
      </nav>
    </transition>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isMobileMenuOpen = ref(false);
const scrolled = ref(false);

const handleScroll = () => {
  scrolled.value = window.scrollY > 10;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
  document.body.style.overflow = "";
});

watch(isMobileMenuOpen, (val) => {
  if (val) {
    document.body.style.overflow = "hidden";
  } else {
    document.body.style.overflow = "";
  }
});
</script>

<style scoped>
.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.3s ease-in-out;
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

line {
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), opacity 0.4s ease;
  transform-origin: center;
}

/* Transformation des barres en croix */

.transform-top {
  transform: rotate(45deg) translate(0px, 6px);
}

.transform-bottom {
  transform: rotate(-45deg) translate(0px, -6px);
}
</style>
