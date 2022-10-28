<template>
  <div>
    <Hero></Hero>
    <Sponsors></Sponsors>
    <MinCategory></MinCategory>
    <CourseSlider></CourseSlider>
    <BundleCourse></BundleCourse>
    <cohorts></cohorts>
    <proplan></proplan>
  </div>
</template>

<script>
import Hero from '@/components/Home/components/Hero.vue'
import Sponsors from '@/components/Home/components/Sponsors.vue'
import MinCategory from '@/components/Home/components/MinCategory.vue'
import CourseSlider from '@/components/Home/components/CourseSlider.vue'
import BundleCourse from '@/components/Home/components/BundleCourse.vue'
import cohorts  from "@/components/Home/components/cohorts.vue"
import proplan  from "@/components/Home/components/proplan.vue"
export default {
    name: 'index',
    components:{
      Hero,
      Sponsors,
      MinCategory,
      CourseSlider,
      BundleCourse,
      cohorts,
      proplan
    }
}
</script>

<style scoped>

</style>