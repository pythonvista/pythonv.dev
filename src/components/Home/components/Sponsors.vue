<template>
  <div class="wrap bg-primary py-3 flex flex-col justify-center gap-2 align-center">
    <div class="sponsor_title">
        <p class="ma-0 pa-0 text-white">Our Company and Sponsors</p>
    </div>
    <div  class="sponsors_img flex xs:flex-col sm:flex-col md:flex-row lg:flex-row items-center justify-center xs:gap-5 md:gap-5">
        <img  src="@/assets/img/companyLogo/nablintech.png" alt="">
        <img src="@/assets/img/companyLogo/carbonwurld.png" alt="">
        <img src="@/assets/img/companyLogo/kinplus.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
    name: 'Sponsors'

}
</script>

<style scoped>
.sponsors_img img{
    width: 10%;
}

.wrap{
    overflow: hidden;
}
@media (max-width: 640px) {
    .sponsors_img img{
    width: 20%;
}
.sponsors_img{
    flex-direction: row !important;
}

}

</style>