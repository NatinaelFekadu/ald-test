<template>
  <div class="bg-white rounded-lg max-w-4xl" :style="{ marginLeft: '10.5%', maxWidth: '700px' }">
    <div class="space-y-4">
      <!-- Description Header -->
      <h2 class="text-2xl font-semibold text-gray-800">Description</h2>
      
      <!-- Static Paragraphs (always visible) -->
      <div class="space-y-4 text-sm">
        <p>
          In today’s rapidly evolving world, driven by AI and constant disruptions, the need for stability in your career or business has 
          never been more challenging. Whether you're looking to innovate within your organization, advance in your career, or start your own venture, 
          adapting and thriving are no longer optional—they’re essential.
        </p>
        <p>
          Developed by an entrepreneur with over 20 years of experience across 5 different industries, this course uniquely 
          equips you with the entrepreneurial mindset, strategies, and tools needed to navigate today’s unpredictable business landscape,
          advance your career and company, or launch a new venture. You’ll learn how to turn challenges into opportunities and secure a prosperous, resilient future.
        </p>
      </div>
      
      <!-- Toggleable Content -->
      <div v-if="showMore" class="space-y-4">
        <h3 class="text-xl font-semibold text-gray-800">Master the Skills to Adapt, Innovate and Excel in an Ever-Changing World</h3>
        <ul class="list-disc pl-5 space-y-2 text-sm">
          <li>Gain Exclusive Access to Proven Tools and Techniques from 20 Years of Multi-Industry Experience</li>
          <li>Develop Behavioral Skills to Extract Unparalleled Critical Insights from Users and Customers</li>
          <li>Master Strategic Methods to Turn Competition into Unique Advantages</li>
          <li>Unlock Hard-Earned, Experience-Based Strategies from Exclusive Multi-Industry Case Studies</li>
        </ul>
        
        <h3 class="text-xl font-semibold text-gray-800">Who this course is for?</h3>
        <p class="text-sm">
          This course is designed for a diverse group of learners who want to advance their careers, 
          launch ventures, or drive innovation:
        </p>
        <ul class="list-disc pl-5 space-y-2 text-sm">
          <li>Aspiring entrepreneurs looking to launch, grow, or improve a business, even with no prior experience.</li>
          <li>Intrapreneurs aiming to drive innovation and growth within their organizations.</li>
          <li>Product managers and product marketers wanting to understand market needs, validate demand, and develop a competitive edge.</li>
          <li>Business owners and entrepreneurs seeking to adapt to disruption and make informed strategic decisions.</li>
          <li>Professionals interested in leveraging human behavioral insights to improve decision-making and entrepreneurial success.</li>
        </ul>
      </div>
      
      <!-- Show More/Show Less Button -->
      <div class="mt-4 flex">
        <button @click="toggleShowMore" class="text-sm font-bold mb-5 text-indigo-700 hover:text-blue-700">
          <span v-if="showMore">Show Less</span>
          <span v-else>Show More </span>
        </button>
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMore: false,
    };
  },
  methods: {
    toggleShowMore() {
      this.showMore = !this.showMore;
    },
  },
};
</script>

<style scoped>
/* Optional additional styles */
</style>
