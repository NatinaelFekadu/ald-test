<!-- CourseInfoCard.vue -->
<template>
    <div class="flex items-center bg-white border rounded-lg p-4 max-w-2xl shadow-sm mb-4">
      <!-- Course Image -->
      <img
        :src="image"
        alt="Course Thumbnail"
        class="w-16 h-16 rounded-lg object-cover mr-4"
      />
  
      <!-- Course Details -->
      <div class="flex-1">
        <!-- Title and Rating Row -->
        <div class="flex items-center justify-between">
          <h2 class="text-lg font-bold text-gray-800">{{ title }}</h2>
          <div class="flex items-center">
            <span class="text-sm font-medium text-gray-800 mr-1">{{ rating }}</span>
            <svg
              class="h-5 w-5 text-yellow-500"
              fill="currentColor"
              viewBox="0 0 20 20"
            >
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.342 4.124a1 1 0 00.95.69h4.345c.969 0 1.371 1.24.588 1.81l-3.51 2.52a1 1 0 00-.364 1.118l1.342 4.124c.3.921-.755 1.688-1.54 1.118l-3.51-2.52a1 1 0 00-1.176 0l-3.51 2.52c-.784.57-1.838-.197-1.539-1.118l1.342-4.124a1 1 0 00-.364-1.118l-3.51-2.52c-.783-.57-.38-1.81.588-1.81h4.345a1 1 0 00.95-.69l1.342-4.124z" />
            </svg>
          </div>
        </div>
  
        <!-- Additional Info Row -->
        <div class="flex items-center text-sm text-gray-600 mt-1">
          <span v-if="isPremium" class="bg-purple-600 text-white px-2 py-0.5 rounded-md mr-2 font-semibold text-xs">
            Premium
          </span>
          <span class="mr-2">{{ duration }}</span>
          <span class="mr-2">•</span>
          <span>Updated {{ lastUpdate }}</span>
        </div>
      </div>
  
      <!-- Enrollment and Price -->
      <div class="flex ml-4">
        <span class="text-gray-600 text-sm flex mt-1 mr-4">
          <img src="../public/users.png" class="w-4 h-4"/>
          <span class="pl-1">
              {{ enrollmentCount }}
          </span>
        </span>
        <span class="text-lg font-semibold text-gray-800 mr-2">${{ price }}</span>
        <button class="text-gray-500 hover:text-red-500 transition rounded-full p-3 border border-black">
            <img src="../public/fav.svg" class="w-5 h-5" />
        </button>

      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CourseInfoCard',
    props: {
      image: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      },
      rating: {
        type: Number,
        required: true
      },
      enrollmentCount: {
        type: Number,
        required: true
      },
      price: {
        type: Number,
        required: true
      },
      duration: {
        type: String,
        required: true
      },
      lastUpdate: {
        type: String,
        required: true
      },
      isPremium: {
        type: Boolean,
        default: false
      }
    }
  };
  </script>
  
  <style scoped>
  .shadow-sm {
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  }
  </style>
  