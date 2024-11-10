<template>
    <div>
        <SmartBar />
        <UdemyHeader />
        <Nuxt />
    </div>
  </template>
  
  <script>
  import UdemyHeader from '~/components/UdemyHeader.vue';
  import SmartBar from '~/components/SmartBar.vue';
  
  export default {
    components: {
      UdemyHeader,
    },
  }
  </script>
  