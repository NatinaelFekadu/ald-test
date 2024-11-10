<template>
  <header class="flex justify-between items-center px-6 bg-white border-b pl-4">
    <!-- Left Section: Categories and Login -->
    <div class="flex items-center space-x-4">
      <!-- Categories Dropdown -->
      <div class="flex items-center">
          <nuxt-link to="/" class="flex items-center">
            <img
              src="../public/udemy_logo.svg"
              alt="Udemy"
              class="w-24 h-auto"
            />
          </nuxt-link>
        </div>
      <div class="relative group">
        <button class="text-sm font-medium text-gray-700 flex items-center">
          <span>Categories</span>
        </button>
        <!-- Dropdown Menu (visible only on hover) -->
        <div
          class="absolute mt-2 w-48 bg-white border rounded shadow-lg z-10 opacity-0 group-hover:opacity-100 transform scale-95 group-hover:scale-100 transition-all duration-200"
        >
          <ul class="py-2">
            <li>
              <nuxt-link to="/courses/development" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Development</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/courses/business" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Business</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/courses/finance-and-accounting" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Finance & Accounting</nuxt-link>
            </li>
          </ul>
        </div>
      </div>

      <!-- Log In -->
    </div>

    <!-- Middle Section: Search -->
    <div class="flex mx-4 relative w-[450px] ">
  <!-- FontAwesome icon inside the input field -->
        <img src="../public/search_icon.svg" class="absolute left-4 top-1/2 transform -translate-y-1/2 text-gray-400 h-4 w-4" />
        
        <input
            type="text"
            placeholder="Search for anything"
            class="w-full pl-12 pr-4 py-2 border border-black rounded-full focus:outline-none"
        />
    </div>

    <!-- Right Section: Udemy Business & Sign Up -->
    <div class="flex items-center space-x-4">
      <nuxt-link to="/udemy-business" class="text-sm font-medium text-gray-700">Plans & Pricing</nuxt-link>
    </div>
    <div class="flex items-center space-x-4">
      <nuxt-link to="/udemy-business" class="text-sm font-medium text-gray-700">Udemy Business</nuxt-link>
    </div>
    <div class="flex items-center space-x-4">
      <nuxt-link to="/udemy-tech" class="text-sm font-medium text-gray-700">Teach On Udemy</nuxt-link>
    </div>
    <div class="flex items-center space-x-4">
      <button type="button" class="flex items-center hover:bg-gray-200 text-sm font-medium text-gray-700  p-2">
        <!-- Icon inside the button -->
        <nuxt-link to="/" class="flex items-center">
          <img
            src="../public/cart.svg"
            alt="Udemy"
            class="w-6 h-auto"
          />
        </nuxt-link>
      </button>
      <!-- Log In Button -->
      <a
        data-purpose="header-login"
        href="https://www.udemy.com/join/login-popup/?locale=en_US&amp;response_type=html&amp;next=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fmaster-figma-from-beginner-to-pro-in-uiux-design%2F%3FcouponCode%3DST2MT110724BNEW"
        class="ud-btn ud-btn-medium ud-btn-secondary ud-heading-sm text-sm font-medium text-gray-700 border border-black p-2"
      >
        <span class="ud-btn-label">Log in</span>
      </a>

      <!-- Sign Up Button -->
      <a
        href="https://www.udemy.com/join/signup-popup/?locale=en_US&amp;response_type=html&amp;next=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fmaster-figma-from-beginner-to-pro-in-uiux-design%2F%3FcouponCode%3DST2MT110724BNEW"
        class="text-sm font-medium text-white bg-black hover:bg-black[400] py-2 px-4 transition duration-200 ease-in-out"
      >
        Sign up
      </a>

      <!-- Language Icon Button -->
      <button type="button" class="flex items-center hover:bg-gray-200 text-sm font-medium text-gray-700 border border-gray-300 p-2">
        <!-- Icon inside the button -->
        <nuxt-link to="/" class="flex items-center">
          <img
            src="../public/language.svg"
            alt="Udemy"
            class="w-6 h-auto"
          />
        </nuxt-link>
      </button>
    </div>



  </header>
</template>

<script>
export default {
  name: 'UdemyHeader',
}
</script>

<style scoped>
/* Custom styles for responsiveness */
@media (max-width: 768px) {
  .flex-1 {
    max-width: none; /* Remove max-width restriction on smaller screens */
  }
  .mx-4 {
    margin-left: 2rem; /* Add margin on left and right */
    margin-right: 2rem;
  }
}
</style>
