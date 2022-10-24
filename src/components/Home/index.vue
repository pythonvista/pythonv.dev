<template>
  <div>
    <Hero></Hero>
    <Sponsors></Sponsors>
    <MinCategory></MinCategory>
    
  </div>
</template>

<script>
import Hero from '@/components/Home/components/Hero.vue'
import Sponsors from '@/components/Home/components/Sponsors.vue'
import MinCategory from '@/components/Home/components/MinCategory.vue'
export default {
    name: 'index',
    components:{
      Hero,
      Sponsors,
      MinCategory
    }
}
</script>

<style scoped>

</style>