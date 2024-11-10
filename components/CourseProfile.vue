<template>
  <div class="bg-dark p-20 py-7">
    <!-- Breadcrumb Section -->
    <div class="text-white text-lg ml-16">
      <div class="flex space-x-2">
        <a href="/courses/design/" class="text-sm font-semibold text-indigo-200">Business</a>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6l6 6-6 6"/>
        </svg>
        <a href="/courses/design/user-experience/" class="text-sm font-semibold text-indigo-200">Enterpreneurship</a>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6l6 6-6 6"/>
        </svg>
        <a href="/topic/figma/" class="text-sm font-semibold text-indigo-200">Innovation</a>
      </div>
    </div>

    <!-- Main Content Section -->
    <div class="mt-6 ml-10 w-10/12">
      <div class="bg-dark pl-6 rounded-lg mb-6">
        <div class="flex justify-between items-center">
          <div class="w-full md:w-2/3 flex flex-start flex-col">
            <h1 class="text-3xl text-white font-bold mb-4">Adaptive Entrepreneurship: Thriving Through Constant Change</h1>
            <p class="text-white">Drive a quantum leap in your life with expert-led entrepreneurial strategies, behavioral skills and competition tactics</p>
          </div>
          <!-- <div class="hidden md:block w-1/3">
            <img src="https://img-c.udemycdn.com/course/240x135/6080417_89c8_2.jpg" alt="Course Preview" class="w-full h-auto rounded-lg"/>
          </div> -->
        </div>
      </div>

      <!-- Course Price and Rating -->
      <div class="mt-2 pl-6 flex justify-start space-x-2 items-center text-white">
        <button class="bg-blue-200 text-black py-1 px-3 text-sm font-semibold">
            New
        </button>
        <span class="text-yellow-600">4.7</span>
        <img src="../public/5_star.svg" alt="Course Preview" class="w-24 h-auto rounded-lg"/>
        <a href="#"  class="text-indigo-200">(11 ratings)</a>
        <span>25 students</span>
      </div>

      <!-- Instructor Info -->
      <div class="mt-2 pl-6 space-x-2">
        <span class="text-white ">Created by</span>
        <a href="#instructor-1" class="underline text-indigo-200">Hanan Markovich</a>
      </div>

      <!-- Last Update and Language -->
      <div class="mt-4 text-gray-300 text-sm flex flex-row space-x-4 pl-6 mb-6 font-bold">
        <span>Last updated 10/2024</span>
        <span>English</span>
        <span>
            English
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // This page doesn't require any script logic
}
</script>

<style scoped>
.bg-dark {
  background-color: #1C1D1F;
}
.bg-gradient-to-b {
  background: linear-gradient(to bottom, #1f2937, #4b5563);
}
</style>
