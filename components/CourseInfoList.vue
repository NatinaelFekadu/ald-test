<!-- CourseInfoList.vue -->
<template>
    <div class="bg-white rounded-lg max-w-4xl" :style="{ marginLeft: '10.5%', maxWidth: '700px' }">
      <h2 class="text-2xl font-bold mb-6">Students also bought</h2>
      <CourseInfoCard
        v-for="course in courses"
        :key="course.id"
        :image="course.image"
        :title="course.title"
        :rating="course.rating"
        :enrollmentCount="course.enrollmentCount"
        :price="course.price"
        :duration="course.duration"
        :lastUpdate="course.lastUpdate"
        :isPremium="course.isPremium"
      />
    </div>
  </template>
  
  <script>
  import CourseInfoCard from './CourseInfoCard.vue';
  
  export default {
    name: 'CourseInfoList',
    components: {
      CourseInfoCard
    },
    data() {
      return {
        courses: [
          {
            id: 1,
            image: 'https://img-b.udemycdn.com/course/240x135/115440_8349_27.jpg',
            title: 'Strategic Innovation and Execution',
            rating: 4.4,
            enrollmentCount: 55947,
            price: 59.99,
            duration: '4 total hours',
            lastUpdate: '9/2024',
            isPremium: true
          },
          {
            id: 2,
            image: 'https://img-b.udemycdn.com/course/240x135/404944_b3d1_3.jpg',
            title: 'Innovation Master Class',
            rating: 4.7,
            enrollmentCount: 42412,
            price: 69.99,
            duration: '3.8 total hours',
            lastUpdate: '8/2024',
            isPremium: true
          },
          {
            id: 3,
            image: 'https://img-b.udemycdn.com/course/240x135/945766_98d6_2.jpg',
            title: 'Innovation Growth Strategy: A Begginner\'s Guide',
            rating: 4.5,
            enrollmentCount: 101243,
            price: 39.99,
            duration: '10 total hours',
            lastUpdate: '7/2024',
            isPremium: true
          }
        ]
      };
    }
  };
  </script>
  
  