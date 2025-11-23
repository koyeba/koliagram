<script setup lang="ts">
definePageMeta({
  layout: false,
});

// Form state
const username = ref("");
const password = ref("");
const loading = ref(false);
const error = ref("");

// Handle login
const handleLogin = async () => {
  error.value = "";
  loading.value = true;

  try {
    // TODO: Replace with your actual authentication API
    await new Promise((resolve) => setTimeout(resolve, 1000)); // Simulate API call

    // Example login logic (replace with real API)
    console.log("Login attempt:", {
      username: username.value,
      password: password.value,
    });

    // Success - redirect to dashboard or home
    navigateTo("/");
  } catch (e) {
    error.value = "Une erreur est survenue. Veuillez réessayer.";
  } finally {
    loading.value = false;
  }
};
</script>

<template>
  <div class="min-h-screen w-full flex">
    <div
      class="w-full md:w-1/2 flex flex-col gap-4 items-center justify-center px-4 sm:px-6 lg:px-8"
    >
      <NuxtLink to="/">
        <NuxtImg
          src="/img/logo-koliagram.svg"
          alt="Logo Koliagram"
          class="w-40"
        />
      </NuxtLink>
      <div class="text-center mb-8">
        <h1
          class="text-2xl text-gray-900 font-display font-medium tracking-tight"
        >
          Connexion
        </h1>
        <h2 class="text-gray-600 text-xs">Accédez à votre espace personnel</h2>
      </div>

      <!-- Login Form -->
      <form @submit.prevent="handleLogin" class="w-full max-w-md space-y-6">
        <!-- Error Message -->
        <div
          v-if="error"
          class="bg-red-50 border border-red-200 text-red-600 px-4 py-3 rounded-xl text-sm"
        >
          {{ error }}
        </div>

        <!-- Username Field -->
        <div>
          <label
            for="username"
            class="block text-sm font-medium text-gray-700 mb-2"
          >
            Nom d'utilisateur
          </label>
          <input
            id="username"
            v-model="username"
            type="text"
            required
            :disabled="loading"
            class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-[#FF630B] focus:border-transparent transition-all disabled:opacity-50 disabled:cursor-not-allowed"
            placeholder="Entrez votre nom d'utilisateur"
          />
        </div>

        <!-- Password Field -->
        <div>
          <label
            for="password"
            class="block text-sm font-medium text-gray-700 mb-2"
          >
            Mot de passe
          </label>
          <input
            id="password"
            v-model="password"
            type="password"
            required
            :disabled="loading"
            class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-[#FF630B] focus:border-transparent transition-all disabled:opacity-50 disabled:cursor-not-allowed"
            placeholder="Entrez votre mot de passe"
          />
        </div>

        <!-- Submit Button -->
        <button
          type="submit"
          :disabled="loading"
          class="w-full bg-[#FF630B] hover:bg-[#CC5009] text-white font-medium py-3 px-4 rounded-xl transition-colors disabled:opacity-50 disabled:cursor-not-allowed"
        >
          {{ loading ? "Connexion..." : "Se connecter" }}
        </button>

        <!-- Forgot Password Link -->
        <div class="text-center">
          <NuxtLink
            to="/forgot-password"
            class="text-sm text-gray-600 hover:text-[#FF630B] transition-colors"
          >
            Mot de passe oublié ?
          </NuxtLink>
        </div>
      </form>
    </div>
    <div class="hidden md:block w-1/2">
      <NuxtImg
        src="/img/chef.jpg"
        alt="Chef"
        class="w-full h-full object-cover"
      />
    </div>
  </div>
</template>
