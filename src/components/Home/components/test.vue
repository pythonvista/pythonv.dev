<template>
  <!-- Slider main container -->
  <div ref="swiper" class="swiper">
    <!-- Additional required wrapper -->
    <div class="swiper-wrapper">
      <!-- Slides -->
      <div class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
        <div class="circle flex align-center flex-column justify-center items-center">
          <v-icon color="black">mdi-account</v-icon>

        </div>
        <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
          Programing</p>
        <p class="ma-0 pa-0 p2 font-normal text-sm ">5 courses</p>
      </div>
      <div class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
        <div class="circle flex align-center flex-column justify-center items-center">
          <v-icon color="black">mdi-account</v-icon>

        </div>
        <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
          Programing</p>
        <p class="ma-0 pa-0 p2 font-normal text-sm ">5 courses</p>
      </div>
      <div class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
        <div class="circle flex align-center flex-column justify-center items-center">
          <v-icon color="black">mdi-account</v-icon>

        </div>
        <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
          Programing</p>
        <p class="ma-0 pa-0 p2 font-normal text-sm ">5 courses</p>
      </div>
      <div class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
        <div class="circle flex align-center flex-column justify-center items-center">
          <v-icon color="black">mdi-account</v-icon>

        </div>
        <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
          Programing</p>
        <p class="ma-0 pa-0 p2 font-normal text-sm ">5 courses</p>
      </div>
      <div class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
        <div class="circle flex align-center flex-column justify-center items-center">
          <v-icon color="black">mdi-account</v-icon>

        </div>
        <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
          Programing</p>
        <p class="ma-0 pa-0 p2 font-normal text-sm ">5 courses</p>
      </div>
      <div class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
        <div class="circle flex align-center flex-column justify-center items-center">
          <v-icon color="black">mdi-account</v-icon>

        </div>
        <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
          Programing</p>
        <p class="ma-0 pa-0 p2 font-normal text-sm ">5 courses</p>
      </div>
    </div>
    <!-- If we need pagination -->
    <div class="swiper-pagination"></div>

    <!-- If we need navigation buttons -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>

    <!-- If we need scrollbar -->
    <div class="swiper-scrollbar"></div>
  </div>
</template>
<script>
import Swiper, { EffectCards } from 'swiper'
console.log(EffectCards)
import 'swiper/css'
import "swiper/css/effect-cards";

export default {
  mounted() {
    new Swiper(this.$refs.swiper, {
      // configure Swiper to use modules
      modules: [EffectCards],
      // Optional parameters
      // loop: true,
      effect: 'cards',

      // If we need pagination
      // EffectCards:{
      //   effect: 'cards'
      // }
    })
  },
}
</script>

<style scoped>
.category_items {
  background-color: rgb(255, 255, 255);
  border-radius: 20px;
  display: flex !important;
  text-align: center;
  gap: 10px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  line-height: 1rem;
  transition: 0.5s;
  color: black !important;
}

.swiper-scrollbar {
  display: none !important;
}

.category_items:hover {
  background-color: #60109E !important;
  color: white !important ;
  cursor: pointer;
}

.swiper {
  max-width: 130px;
  max-height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 18px;
  font-size: 22px;
  font-weight: bold;
  color: #fff;
  max-width: 130px;
  max-height: 200px;
}



.swiper-button-prev {
  display: none !important;
}

.swiper-button-next {
  display: none !important;
}
</style>