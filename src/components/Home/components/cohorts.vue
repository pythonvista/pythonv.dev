<template>
    <div class="cohort_wrap xs:px-1 sm:px-1 md:px-3 lg:px-3 py-5">
        <div ref="swiper" class="swiper ">
            <div class="swiper-wrapper">

                <div class="swiper-slide" v-for="(n, index) in 9" :key="index">
                    <a href="">Title</a>
                    <div
                        class="contain flex xs:flex-col sm:flex-col md:flex-row lg:flex-row xs:items-center gap-3 md:items-center lg:items-center md:justify-between lg:justify-between">
                        <div class="flex flex-col gap-2">
                            <p class="pa-0 ma-0">Full Stack Engineer Cohort</p>
                            <p class="pa-0 ma-0">12 Months at 70 hours / week | Application deadline : 2
                                December 2023</p>
                        </div>

                        <div>
                            <v-btn small>Notify Me</v-btn>
                        </div>

                    </div>

                </div>
            </div>

            <div class="swiper-button-prev">
                <img src="@/assets/icons/next.png" alt="">
            </div>
            <div class="swiper-button-next">
                <img src="@/assets/icons/next.png" alt="">
            </div>
        </div>




    </div>
</template>

<script>
import Swiper, { Pagination, Navigation } from 'swiper'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
export default {
    name: 'cohorts',
    mounted() {
        new Swiper(this.$refs.swiper, {
            // configure Swiper to use modules
            modules: [Pagination, Navigation],
            loop: true,
            slidesPerView: 1,
            pagination: {
                el: '.swiper-pagination',
            },
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },

            // And if we need scrollbar
            scrollbar: {
                el: '.swiper-scrollbar',
            },
        })

    }

}
</script>

<style scoped>
.cohort_wrap {
    background: #D6CDDC;

}

.swiper {
    max-width: 80%;
    height: 150px;
    display: flex;
    background: #60109E;
    align-items: center;
    justify-content: center;

}

.swiper-wrapper {
    position: relative;

}

.swiper-slide a {
    text-decoration: none;
    position: absolute;
    top: 0;
    left: 0;
    padding: 0.3em 2em;
    background: white;
    color: #60109E;
}

.swiper-slide {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

    position: relative;
}

.contain {
    width: 80%;
    /* border: 1px solid red; */
    color: white;
}


.swiper-button-prev {
    /* border: 1px solid black; */
    /* transform: translateX(-10px); */
    width: 50px;
    height: 50px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    background: #DECEEA;
    padding: 5px;

}

.swiper-button-prev img {
    transform: rotate(180deg);
}

.swiper-button-next {
    /* border: 1px solid black; */
    padding: 5px;
    /* transform: translateX(10px); */
    background: #DECEEA;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    width: 50px;
    height: 50px;

}

.swiper-button-prev::after {
    display: none;

}

.swiper-button-next::after {
    display: none;

}

@media (max-width:640px) {

    .swiper {
        max-width: 94%;
        height: 150px;
        display: flex;
        background: #60109E;
        align-items: center;
        justify-content: center;

    }

    .swiper-button-prev,
    .swiper-button-next{
        width: 30px;
        height: 30px;

        padding: 2.5px;
    }

    .contain{
        padding: 0 1em;
        text-align: center !important;
    }

    .swiper-slide a {
    text-decoration: none;
    position: absolute;
    top: 0;
    left: 0;
    padding: 0.2em 0.6em;
    background: white;
    color: #60109E;
}
}
</style>