<template>
  <div v-if="isVisible" class="bg-[#5c33ce] py-3 pr-10 relative">
    <div class="flex justify-center items-center">
      <div class="text-center">
        <span role="presentation" class="text-black" data-testid="smart-bar-copy">
          <span class="text-white font-bold text-[16px]" data-purpose="smart-bar-title" data-testid="smart-bar-title">
            Ready to get with the times?
          </span>
          <span class="text-white text-[16px]" role="presentation" data-purpose="smart-bar-subtitle" data-testid="smart-bar-subtitle">
            | Get the skills with Udemy Business.
          </span>
        </span>
      </div>
      <!-- Close Button ('X') -->
      <button @click="closeAd" class="absolute right-4 top-1/2 transform -translate-y-1/2 text-white font-bold text-2xl">
        &times;
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SmartBar',
  data() {
    return {
      isVisible: true, // Tracks component visibility
    };
  },
  methods: {
    closeAd() {
      this.isVisible = false; // Hides component when button is clicked
    },
  },
};
</script>

<style scoped>
/* Custom styles or Tailwind extensions can go here if needed */
</style>
