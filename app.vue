<template>
  <div>
    <Promotion />
    <Header />
    <div class="relative">
      <div class="relative">
        <CourseProfile class="w-full" /> 
        <CoursePreview class="absolute top-10 right-[100px]" />
      </div>
    </div>
    <CourseOutcomes/>
    <CourseTopics/>
    <CourseMainContent/>
    <CourseRequirements/>
    <CourseDescription/>
    <CourseInfoList />
  </div>
</template>

<style scoped>
.relative {
  position: relative;
}

.absolute {
  position: absolute;
}

.z-10 {
  z-index: 10;
}
</style>
