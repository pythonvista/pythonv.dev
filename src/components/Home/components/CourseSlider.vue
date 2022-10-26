<template>
    <div class="course_wrap xs:px-2 sm:px-2 md:px-7 lg:px-7  ">
        <img class="wave" src="@/assets/img/bg.svg" alt="">
        <img class="wavemob" src="@/assets/img/course-bg.svg" alt="">
        <div class="category_title flex flex-column ">
            <!-- <p
                class="text-primary font-medium text-sm ma-0 pa-0 xs:text-center sm:text-center md:text-left lg:text-left ">
                Popular Category</p> -->
            <div class="relative gap-3 mt-2 mb-2 flex xs:flex-col sm:flex-col md:flex-row lg:flex-row align-center">
                <p class="font-bold   ma-0 pa-0">Popular Courses</p>
            </div>
        </div>
        <div ref="swiper" class="swiper">
            <!-- Additional required wrapper -->
            <div class="swiper-wrapper">
                <!-- Slides -->
                <div class="swiper-slide" v-for="(n, index) in 9" :key="index">
                    <div class="shadow-lg bg-white focus-within:shadow-md hover:shadow-2xl course_slide flex items-center flex-col ">
                        <div class="course_img w-full">
                            <img src="@/assets/img/course1.png" alt="">
                        </div>
                        <div class="course_content w-full flex flex-col ">
                            <div class="course_info flex flex-col justify-center gap-1 pa-1">
                                <p class="ma-0 pa-0 text-bold text-primary font-bold">Node JS Crash Course</p>
                                <p class="ma-0 pa-0 text-xs">Learn how to make dynamic websites
                                    using Node ja and firebase from ground.</p>
                            </div>
                            <div class="course_price flex flex-row justify-between items-center ">
                                <div class="flex flex-row items-center gap-1">
                                    <div class="avatar">
                                        <img src="@/assets/img/avatar.png" alt="">
                                    </div>
                                    <div class="avatar_name"><p class="ma-0 pa-0 text-xs">Emeter Victor</p></div>
                                </div>

                                <div class="price flex items-center justify-center">
                                    <span class="text-primary">₦{{5000}}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
               
            </div>
            <!-- If we need pagination -->
            <!-- <div class="swiper-pagination"></div> -->

            <!-- If we need navigation buttons -->
            <div class="swiper-button-prev">
                <img src="@/assets/icons/next.png" alt="">
            </div>
            <div class="swiper-button-next">
                <img src="@/assets/icons/next.png" alt="">
            </div>

            <!-- If we need scrollbar -->
            <!-- <div class="swiper-scrollbar"></div> -->
        </div>

    </div>

</template>

<script>
import Swiper, { Pagination, Navigation } from 'swiper'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
export default {
    name: 'CourseSlide',
    data: () => ({
        size: 4
    }),
    methods: {

        setSize() {
            let currWidth = window.screen.width
            if (currWidth <= 640)  {
                this.size = 1
            }else if(currWidth >=640 && currWidth <= 820) {
                this.size = 2
            }else if(currWidth >=820 && currWidth <= 920){
                this.size = 3
            }else{
                this.size = 4
            }

           
            
        }
    },
    created() {

        this.setSize()
        window.addEventListener('resize', function () {
            let currWidth = window.screen.width
            if (currWidth > 768) {
                this.size = 3
                console.log(currWidth)
            }
            if (currWidth <= 640) {
                this.size = 1
                console.log(currWidth)
            }
        }, true);
    },
    mounted() {
        new Swiper(this.$refs.swiper, {
            // configure Swiper to use modules
            modules: [Pagination, Navigation],
            loop: true,
            slidesPerView: this.size,
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

.course_wrap{
    position: relative ;
    overflow: hidden;
}

.wave {
    position: absolute;
    /* top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%; */
    top: 0;
    left: 0;
    width:100%;
    height:100%;
    object-fit: cover;
}

.wavemob {
    display: none;
}
.swiper-slide {
    display: flex;
    justify-content: center;
    align-items: center;
    /* border: 1px solid black; */
    padding: 10px 0;
}

/* .swiper-wrapper{
    display: flex ;
    gap: 10px;
} */
.course_slide {
    height: 380px;
    width: 220px;
    padding: 8px;
    border-radius: 30px;
    overflow: hidden;
}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.course_img {
    height: 70% !important;

    border-radius: 20px;
    overflow: hidden;
}

.course_img img {
    object-fit: cover;
}

.course_content {
    /* border: 1px solid black;s */
    height: 30%;
}

.course_price {
    /* border: 1px solid red; */
    padding: 0 7px 2px 0;
}

.avatar {
    width: 28px;
    height: 28px;
    background-color: #FEF5E4;
    border-radius: 50%;
    overflow: hidden ;
}

.avatar img{
    width: 100%;
    object-fit: cover;
    /* display: none; */
}



.price {
    min-width: 60px;
    min-height: 24px;
    background: #DECEEA;
    border: 2px dashed #8246B0;

}

.swiper-button-prev{
    /* border: 1px solid black; */
    transform: translateX(-10px);
    width: 50px;
    height: 50px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius:50% ;
    background: #DECEEA;
    padding: 5px;

}

.swiper-button-prev img{
    transform: rotate(180deg);
}
.swiper-button-next{
    /* border: 1px solid black; */
    padding: 5px;
    transform: translateX(10px);
    background: #DECEEA;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius:50% ;
    width: 50px;
    height: 50px;

}
.swiper-button-prev::after{
    display: none;

}

.swiper-button-next::after{
    display: none;

}

@media (max-width: 640px) {
.wave{
    display: none;
}

.wavemob{
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