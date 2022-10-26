<template>
  <div>
    <Hero></Hero>
    <Sponsors></Sponsors>
    <MinCategory></MinCategory>
    <CourseSlider></CourseSlider>
    <BundleCourse></BundleCourse>
  </div>
</template>

<script>
import Hero from '@/components/Home/components/Hero.vue'
import Sponsors from '@/components/Home/components/Sponsors.vue'
import MinCategory from '@/components/Home/components/MinCategory.vue'
import CourseSlider from '@/components/Home/components/CourseSlider.vue'
import BundleCourse from '@/components/Home/components/BundleCourse.vue'
export default {
    name: 'index',
    components:{
      Hero,
      Sponsors,
      MinCategory,
      CourseSlider,
      BundleCourse
    }
}
</script>

<style scoped>

</style>