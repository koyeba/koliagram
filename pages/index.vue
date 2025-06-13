<template>
  <div>
    <div class="h-auto mb-40">
      <div
        class="flex flex-col gap-10 pt-35 lg:pt-50 text-center items-center mb-14 font-display"
      >
        <p class="text-sm bg-gray-100 rounded-full py-2 w-60">
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
        <NuxtLink
          to="/"
          class="px-10 py-4 rounded-full bg-[#FF630B] hover:bg-[#CC5009] transition-colors duration-300 text-white font-semibold"
        >
          Réservez votre démo
        </NuxtLink>
      </div>
      <div class="mb-12 px-6">
        <p class="text-center text-sm font-display">
          Les meilleurs établissement nous font
          <span class="font-bold"
            >confiance pour gérer leur présence en ligne.</span
          >
        </p>
      </div>
      <div
        class="flex gap-1 md:gap-10 justify-between md:justify-center items-center px-6"
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
    <div class="h-screen pt-2">
      <div
        class="flex flex-col items-center text-center gap-5 sm:gap-10 font-display"
      >
        <p class="bg-gray-100 text-sm rounded-full py-2 w-48">
          Prise en main <span class="font-bold text-[#FF630B]">rapide</span>
        </p>
        <h2 class="text-4xl lg:text-5xl font-bold tracking-tighter">
          Découvrez votre <br class="xl:hidden" />
          nouvel allié.
        </h2> 
        <div
          class="w-full max-w-full relative overflow-x-scroll scroll-smooth overflow-y-hidden pl-6 sm:pl-18 md:pl-54 lg:pl-60 xl:pl-70 2xl:pl-120"
          style="scrollbar-width: none; -ms-overflow-style: none"
        >
          <div class="w-full">
            <ul class="grid grid-flow-col auto-cols-max list-none gap-4 pr-10">
              <li
                class="bg-[linear-gradient(to_bottom,rgba(0,0,0,0.9),transparent),url('/background-image-1.jpg')] bg-no-repeat bg-cover h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              >
                <div class="py-6 px-6 text-center">
                  <p
                    class="text-xs lg:text-lg text-white font-semibold font-display text-left"
                  >
                    Rapidité
                  </p>
                  <p
                    class="text-sm lg:text-sm text-white font-semibold text-left"
                  >
                    Installation en 5 min chrono.
                  </p>
                </div>
              </li>
              <li
                class="bg-[linear-gradient(to_bottom,rgba(0,0,0,0.9),transparent),url('/background-image-2.jpg')] bg-no-repeat bg-cover h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              >
                <div class="py-6 px-6 text-center">
                  <p
                    class="text-xs lg:text-lg text-white font-semibold font-display text-left"
                  >
                    Valorisation
                  </p>
                  <p
                    class="text-sm lg:text-sm text-white font-semibold text-left"
                  >
                    Pile à votre image.
                  </p>
                </div>
              </li>
              <li
                class="bg-[linear-gradient(to_bottom,rgba(0,0,0,0.9),transparent),url('/background-image-4.jpg')] bg-no-repeat bg-cover h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              >
                <div class="py-6 px-6 text-center">
                  <p
                    class="text-xs lg:text-lg text-white font-semibold font-display text-left"
                  >
                    Visibilité
                  </p>
                  <p
                    class="text-sm lg:text-sm text-white font-semibold text-left"
                  >
                    Vous n'aurait jamais été aussi visibles.
                  </p>
                </div>
              </li>
              <li
                class="bg-gray-100 h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              ></li>
              <li
                class="bg-gray-100 h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              ></li>
              <li
                class="bg-gray-100 h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              ></li>
              <li
                class="bg-gray-100 h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              ></li>
              <li
                class="bg-gray-100 h-[33rem] md:h-[42rem] xl:h-[46rem] w-[16rem] md:w-[21rem] lg:w-[23rem] rounded-4xl"
              ></li>
              <!-- Padding de fin -->
              <li aria-hidden="true" class="w-2 lg:w-12"></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
