<template>
  <header class="bg-white shadow-lg sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center py-4">
        <!-- Logo -->
        <div class="flex items-center">
          <div class="w-10 h-10 bg-primary-600 rounded-lg flex items-center justify-center mr-3">
            <span class="text-white font-bold text-xl">F</span>
          </div>
          <div>
            <h1 class="text-xl font-bold text-gray-900">FitLife Gym</h1>
            <p class="text-sm text-primary-600 font-medium">Transform Your Life</p>
          </div>
        </div>

        <!-- Phone Number -->
        <div class="hidden md:flex items-center space-x-2 text-primary-600">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
            <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
          </svg>
          <span class="font-semibold">(555) 123-4567</span>
        </div>

        <!-- Navigation -->
        <nav class="hidden md:flex space-x-8">
          <router-link 
            to="/" 
            class="text-gray-700 hover:text-primary-600 font-medium transition-colors duration-200"
            active-class="text-primary-600"
          >
            Home
          </router-link>
          <router-link 
            to="/book" 
            class="text-gray-700 hover:text-primary-600 font-medium transition-colors duration-200"
            active-class="text-primary-600"
          >
            Book Session
          </router-link>
          <router-link 
            to="/about" 
            class="text-gray-700 hover:text-primary-600 font-medium transition-colors duration-200"
            active-class="text-primary-600"
          >
            About
          </router-link>
        </nav>

        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button 
            @click="toggleMobileMenu"
            class="text-gray-700 hover:text-primary-600 p-2"
          >
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="mobileMenuOpen" class="md:hidden py-4 border-t border-gray-200">
        <div class="flex flex-col space-y-4">
          <router-link 
            to="/" 
            class="text-gray-700 hover:text-primary-600 font-medium transition-colors duration-200"
            active-class="text-primary-600"
            @click="mobileMenuOpen = false"
          >
            Home
          </router-link>
          <router-link 
            to="/book" 
            class="text-gray-700 hover:text-primary-600 font-medium transition-colors duration-200"
            active-class="text-primary-600"
            @click="mobileMenuOpen = false"
          >
            Book Session
          </router-link>
          <router-link 
            to="/about" 
            class="text-gray-700 hover:text-primary-600 font-medium transition-colors duration-200"
            active-class="text-primary-600"
            @click="mobileMenuOpen = false"
          >
            About
          </router-link>
          <div class="flex items-center space-x-2 text-primary-600 pt-2">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
            </svg>
            <span class="font-semibold">(555) 123-4567</span>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      mobileMenuOpen: false
    }
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    }
  }
}
</script>
