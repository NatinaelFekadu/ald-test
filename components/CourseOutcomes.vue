<template>
    <div class="container p-8 bg-white shadow-lg border border-gray-300  h-[360px]">
      <h2 class="text-2xl font-bold mb-6">What you'll learn</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <!-- Left Column with 5 outcomes -->
        <ul class="space-y-2">
          <li
            v-for="(item, index) in outcomes.slice(0, 5)"
            :key="index"
            class="flex items-start space-x-3"
          >
            <!-- Tick Icon -->
            <svg
              aria-hidden="true"
              focusable="false"
              class="w-5 h-5 text-black flex-shrink-0"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M5 13l4 4L19 7"
              />
            </svg>
            <!-- Objective Text -->
            <span class="text-sm text-gray-700">{{ item }}</span>
          </li>
        </ul>
  
        <!-- Right Column with 5 outcomes -->
        <ul class="space-y-2">
          <li
            v-for="(item, index) in outcomes.slice(5)"
            :key="index + 5"
            class="flex items-start"
          >
            <!-- Tick Icon -->
            <svg
              aria-hidden="true"
              focusable="false"
              class="w-5 h-5 text-black flex-shrink-0"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M5 13l4 4L19 7"
              />
            </svg>
            <!-- Objective Text -->
            <span class="text-sm text-gray-700">{{ item }}</span>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        outcomes: [
          "Master the skills to adapt, innovate, and excel in an ever-changing world.",
          "Gain practical tools and behavioral insights to navigate uncertainties with confidence.",
          "Develop and refine value propositions that adapt to customer feedback.",
          "Build resilience and adaptability by mastering the art of pivoting.",
          "Leverage 20+ years of experience across multiple industries to gain insights that accelerate your entrepreneurial journey.",
          "Create strategies to outperform your competition and leverage market shifts.",
          "Identify market needs and validate demand using proven methodologies.",
          "Learn from diverse real-world case studies of success and failure.",
          "Cultivate an entrepreneurial mindset that drives innovation and strategic thinking.",
        
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .container {
    max-width: 700px;
    margin-top: 40px;
    margin-bottom: 40px;
    margin-left: 8.5%;
  }
  </style>
  