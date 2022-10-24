<template>
    <div class="hero px-7  flex items-center justify-center ">
        <img class="eclipse eclipse_left" src="@/assets/img/eclpise_left.svg" alt="">
        <img class="eclipse eclipse_right" src="@/assets/img/eclpise_right.svg" alt="">
        <div class="hero-wrap w-full sm:grid-cols-1 md:grid-cols-3 lg:grid-cols-3 gap-3 grid ">
            <div
                class="hero_title flex md:col-span-2 lg:col-span-2  justify-center xs:items-center xs:order-last sm:order-last md:order-none lg:order-none  flex-col gap-4 sm:items-center md:items-start lg:items-start">
                <h1
                    class=" title_text xs:text-2xl sm:text-2xl md:text-4xl lg:text-4xl  xs:text-center sm:text-center md:text-left lg:text-left font-bold">
                    {{currentHero.title}} <br><span class="text-primary"> {{currentHero.action}}</span>
                </h1>
                <form
                    class="flex w-9/12 xs:items-center sm:items-center md:items-start lg:items-start  md:justify-start lg:justify-start xs:gap-1 sm:gap-1 md:gap-0 lg:gap-0   xs:flex-col sm:flex-col md:flex-row lg:flex-row">
                    <input type="text"
                        class="search_input  border-solid border-2  px-2 md:rounded-l-sm lg:rounded-l-sm border-primary "
                        placeholder="Search Our 3000+ Course">
                    <div class="flex justify-center align-center  h-full">
                        <a href="#" class="search_btn px-2 w-full h-full white--text">Search</a>
                    </div>

                </form>
                <a href="#" class="ma-0 pa-0 black--text underline">Explore courses</a>
            </div>
            <div data-aos="fade-left"
                class="hero_image  flex itemes-center  justify-center md:col-span-1 lg:col-span-1">
                <img class="shadow" :src="currentHero.img">
            </div>
        </div>


    </div>
</template>

<script>
export default {
    name: 'Hero',

    data: () => ({
        currentHero: { title: "Start Learning From", action: "Africa's Best Learning Platform", img: 'system/img/hero2.jpg' },
        start: 0,
        heroContent: [
            {
                title: "Start Learning From ",
                action: "Africa's Best Learning Platform",
                img: 'system/img/hero2.jpg'
            },
            {
                title: "Build Interactive And Beautiful",
                action: "Apps With Python V",
                img: 'system/img/hero3.jpg'
            },
            {
                title: "Computer Programing Concept",
                action: "With Javascript & Python",
                img: 'system/img/hero4.png'
            },

        ]

    }),
    methods: {
        randomHero() {
            setInterval(() => {
                if (this.start <= this.heroContent.length) {
                    this.currentHero = this.heroContent[this.start]
                    this.start += 1
                } else {
                    this.start = 0
                }
            }, 10000)
        }
    },
    created() {
        this.randomHero()
    }

}
</script>

<style scoped>
.hero {
    min-height: 87vh;
    overflow: hidden;
    position: relative;
}

.eclipse {
    position: absolute;
    width: 14%;
    z-index: 1 !important;
}

.eclipse_left {
    top: -20px;
    transform: rotate(20deg);
    left: -40px;
}

.eclipse_right {
    bottom: -20px;
    /* transform: rotate(20deg); */
    right: -40px;
}

.hero-wrap {
    z-index: 2;
}

.search_input {
    width: 70%;
    outline: none;

}

.search_btn {
    background: #60109E;
    display: block;
}

.hero_image {
    overflow: hidden;

}

.hero_image img {
    /* width: 80%; */
    object-fit: contain;

    border-radius: 8px;
}

.title_text {
    line-height: 60px !important;
}

@media (max-width: 640px) {

    .search_input {
        width: 100%;

    }

    .eclipse {
        position: absolute;
        width: 29%;
        z-index: 1 !important;
    }

    .eclipse_left {
        top: -20px;
        transform: rotate(20deg);
        left: -40px;
    }

    .eclipse_right {
        bottom: -80px;
        /* transform: rotate(20deg); */
        right: -30px;
    }

    .hero {
        min-height: 85vh;
        overflow: hidden;
        position: relative;
    }

    .title_text {
        line-height: normal !important;
    }

}
</style>