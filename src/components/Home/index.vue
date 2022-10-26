<template>
  <div>
    <Hero></Hero>
    <Sponsors></Sponsors>
    <MinCategory></MinCategory>
    <CourseSlider></CourseSlider>
    
  </div>
</template>

<script>
import Hero from '@/components/Home/components/Hero.vue'
import Sponsors from '@/components/Home/components/Sponsors.vue'
import MinCategory from '@/components/Home/components/MinCategory.vue'
import CourseSlider from '@/components/Home/components/CourseSlider.vue'
export default {
    name: 'index',
    components:{
      Hero,
      Sponsors,
      MinCategory,
      CourseSlider
    }
}
</script>

<style scoped>

</style>