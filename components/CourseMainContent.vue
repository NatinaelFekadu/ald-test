<template>
  <div class="max-w-4xl p-6" :style="{ marginLeft: '7.5%', maxWidth: '750px' }">
    <h2 class="text-2xl font-bold mb-4">Course content</h2>
    <div class="flex justify-between items-center mb-4">
      <span class="text-sm text-gray-600">11 sections • 60 lectures • 5h 50m total length</span>
      <button @click="toggleExpandAll" class="text-sm font-bold text-indigo-600 hover:underline">
        {{ isExpanded ? 'Collapse all sections' : 'Expand all sections' }}
      </button>
    </div>

    <div class="bg-gray-50 border rounded-lg">
      <div v-for="section in sections" :key="section.title" class="border-b last:border-0">
        <!-- Section Header -->
        <div class="flex justify-between items-start px-4 py-3 cursor-pointer hover:bg-gray-100" @click="section.isOpen = !section.isOpen">
          <div class="flex items-center flex-1">
            <svg
              :class="section.isOpen ? 'transform rotate-180' : ''"
              class="h-5 w-5 text-gray-500 mr-2 transition-transform"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
            <h3 class="text-md font-semibold flex-1">{{ section.title }}</h3>
          </div>
          <span class="text-sm text-gray-500 flex-shrink-0">{{ section.totalDuration }}</span>
        </div>

        <!-- Section Content (Lectures) -->
        <div v-if="section.isOpen" class="px-6 py-3 bg-white">
          <ul>
            <li v-for="lecture in section.lectures" :key="lecture.title" class="flex justify-between items-center py-2 border-b last:border-0">
              <div class="flex items-center">
                <svg class="h-4 w-4 text-gray-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132a1 1 0 00-1.555.832v4.264a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
                <span class="text-sm">{{ lecture.title }}</span>
              </div>
              <span class="text-sm text-gray-500">{{ lecture.duration }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isExpanded: false,
      sections: [
        {
          title: 'Introduction',
          isOpen: false,
          totalDuration: '2 lectures • 17min',
          lectures: [
            { title: 'Welcome: Meet Your Instructor & Course Overview', duration: '03:28' },
            { title: 'Article: Introduction to Adaptive Entrepreneurship', duration: '13:20' },
          ],
        },
        {
          title: 'Thriving in the Era of Constant Change and Creative Destruction',
          isOpen: false,
          totalDuration: '8 lectures • 39min',
          lectures: [
            { title: 'The Era of Disruption and Rapid Changes', duration: '03:13' },
            { title: 'Article: The Era of Disruption and Rapid Changes', duration: '06:05' },
            { title: 'The Era of Disruption and Rapid Changes', duration: '10 questions' },
          ],
        },
        {
          title: 'Becoming an Adaptive Entrepreneur and Identifying Market Needs',
          isOpen: false,
          totalDuration: '6 lectures • 32min',
          lectures: [
            { title: 'Unlocking Customer Insights by Mastering Interviews', duration: '04:05' },
            { title: 'Article: Unlocking Customer Insights by Mastering Interviews', duration: '10 questions' },
          ],
        },
        {
          title: 'Unleashing Innovation: Solving Problems and Defining Winning Solutions',
          isOpen: false,
          totalDuration: '4 lectures • 15min',
          lectures: [
            { title: 'Uncovering Root Causes with the "Five Whys" Method', duration: '03:12' },
            { title: 'Article: Uncovering Root Causes with the "Five Whys" Method', duration: '05:36' },
          ],
        },
      ],
    };
  },
  methods: {
    toggleExpandAll() {
      this.isExpanded = !this.isExpanded;
      this.sections.forEach((section) => {
        section.isOpen = this.isExpanded;
      });
    },
  },
};
</script>

<style scoped>
.bg-gray-50 {
  background-color: #f9fafb;
}

.border {
  border-color: #e5e7eb;
}

.border-b {
  border-bottom: 1px solid #e5e7eb;
}

.rounded-lg {
  border-radius: 8px;
}

.transition-transform {
  transition: transform 0.3s ease;
}

.hover\:bg-gray-100:hover {
  background-color: #f3f4f6;
}
</style>
