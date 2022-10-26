<template>
    <div class="category_wrap px-7 py-3 ">
        <img class="wave" src="@/assets/img/bg-right.svg" alt="">
        <img class="wavemob" src="@/assets/img/bgmob-right.svg" alt="">
        <div class="category_title flex flex-column ">
            <div class="relative gap-3 mt-2 mb-2 flex xs:flex-col sm:flex-col md:flex-row lg:flex-row align-center">
                <p class="font-bold text-primary ma-0 pa-0">Popular Category For Learning</p>

                <select
                    class="text-gray-900 text-sm focus:ring-blue-500 focus:border-blue-500 block p-2.5 dark:focus:ring-blue-500 dark:focus:border-blue-500"
                    placeholder="kndslld">
                    <option v-for="(items, index) in categoryItems" :value="items" :key="index">{{ items }} </option>
                </select>

            </div>
            <div
                class="xs:hidden category_md_lg py-4 px-3 mt-5 mb-6 sm:hidden md:grid lg:grid gap-3 md:grid-cols-3 lg:grid-cols-6 place-items-center content-center">
                <div  v-for="(n, index) in 6" :key="index" class="category_items hover:bg-primary grid-cols-1  card shadow-lg ">
                    <div class="circle flex align-center flex-column justify-center items-center">
                        <v-icon color="black">mdi-account</v-icon>

                    </div>
                    <p class="ma-0 pa-0 font-bold">Computer
                        Programing</p>
                    <p class="ma-0 pa-0 font-normal text-sm">5 courses</p>
                </div>
            </div>
            <div class="xs:flex sm:flex md:hidden lg:hidden md:mt-6 lg:mt7 mb-2">
                <div ref="swiper" class="swiper">
                    <!-- Additional required wrapper -->
                    <div class="swiper-wrapper">
                        <!-- Slides -->
                        <div  v-for="(n, index) in 9" :key="index" class="swiper-slide category_items hover:bg-primary grid-cols-1  card shadow-lg ">
                            <div class="circle flex align-center flex-column justify-center items-center">
                                <v-icon color="black">mdi-account</v-icon>

                            </div>
                            <p class="ma-0 pa-0 p1 font-bold text-base  ">Computer
                                Programing</p>
                            <p class="ma-0 pa-0 p2 font-normal text-sm ">{{index + 12}} courses</p>
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
            </div>

            <a href="#" style="color:#60109E;"
                class="text-primary all-c text-center font-medium text-sm ma-0 pa-0 underline mt-2 ">Explore all
                categories</a>
        </div>
    </div>
</template>

<script>
import Swiper, { EffectCards } from 'swiper'

import 'swiper/css'
import "swiper/css/effect-cards";
export default {
    name: "MinCategory",
    components: {

    },

    data: () => ({
        categoryItems: ['Degrees', 'Course', 'Cohorts', 'Specialization'],


    }),
    mounted() {
        new Swiper(this.$refs.swiper, {
            // configure Swiper to use modules
            modules: [EffectCards],
            effect: 'cards',
        })
    },

}
</script>

<style scoped>
.category_wrap {
    min-height: 65vh ;
    /* display: flex;
    justify-content: start;
    align-items: center;  */
    border-bottom: 4px solid #60109E;
    position: relative;
    overflow: hidden;
    background: #f9f9f9;
}

select {
    outline: none;
    border-bottom: 1px solid #60109E;
    color: black;
    padding: 0 0;
    font-size: 12px;
    background: url("data:image/svg+xml,<svg height='10px' width='10px' viewBox='0 0 16 16' fill='%23000000' xmlns='http://www.w3.org/2000/svg'><path d='M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z'/></svg>") no-repeat;
    background-position: calc(100% - 0.35rem) center !important;
    -moz-appearance: none !important;
    -webkit-appearance: none !important;
    appearance: none !important;
    padding-right: 2rem !important;
}

select option {
    padding: 0 5px !important;

}
.category_title {
    z-index: 2;
}
.all-c{
    z-index: 2 !important;
}

.category_items {
    max-width: 130px;
    min-height: 180px;
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
    z-index: 2;
}

.category_items:hover {
    background-color: #60109E;
    color: white !important;
    cursor: pointer;
}

.selected {
    background: #60109E;
}

.circle {
    width: 2.5rem;
    height: 2.5rem;
    background-color: #FEF5E4;
    border-radius: 50%;
}

.category_md_lg {
    grid-column-gap: 0px !important;
    width: 100%;
}



.swiper-scrollbar {
    display: none !important;
}

.category_items:hover {
    background-color: #60109E !important;
    color: white !important;
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

.swiper-pagination,
.swiper-pagination-bullets,
.swiper-pagination-horizontal {
    display: none !important;
}
.wave {
    position: absolute;
    top: 0;
    left: 0;
    width:100%;
    height:100%;
    object-fit: cover;
}

.wavemob {
    display: none;
}
@media (max-width: 640px) {
    .category_wrap {
        min-height: 55vh;
        display: flex;
        justify-content: center;
        align-items: center;
        border-bottom: 4px solid #60109E;
    }

    .wave {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        display: none;
    }

    .wavemob {
        display: block;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        /* height: 100%; */
        z-index: 0;
    }

}
</style>