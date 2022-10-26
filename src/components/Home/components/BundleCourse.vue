<template>
    <div class="flex flex-column justify-center align-center gap-2 px-4 py-2">
        <div>
            <p class="font-bold text-primary ma-0 pa-0">Bundle Courses</p>
        </div>
        <div class="grid grid-cols-3 w-full place-items-center mt-3 mb-3 gap-2">
            <div v-for="(bundle, index) in bundles" :key="index" class="bundle xs:col-span-3 sm:col-span-3 md:col-span-1 lg:col-span-1 flex flex-column  ">
                <div class="bundle_img ">
                    <img :src="bundle.img" alt="">
                </div>
                <div class="bundle_content  w-full flex flex-col">
                    <div class="bundle_info flex flex-col justify-center gap-1 pa-1">
                        <p class="ma-0 pa-0 text-bold text-primary font-bold">{{bundle.title}}</p>
                        <p class="ma-0 pa-0 text-xs">{{bundle.content}}</p>
                    </div>
                    <div class="bundle_price flex flex-row justify-between items-center px-1 py-2 ">
                        <div class="info flex flex-row items-center justify-center">
                            <span class="">{{bundle.courses}} Courses</span>
                        </div>

                        <div class="price flex items-center justify-center">
                            <span class="text-primary">₦{{ bundle.price }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>

</template>

<script>
export default {
    name: 'bundle',
    data: ()=>({
        bundles: [
            {
                img: require('@/assets/img/bundle/node-crash-course-cover.png'),
                title: 'Node JS Crash Course',
                content: 'Learn how to make dynamic websites using Node js and firebase from ground.',
                price: 5000,
                courses: 23
            },
            {
                img: require('@/assets/img/bundle/mongodb.png'),
                title: 'Leran Mongo Db',
                content: 'Learn how to make dynamic websites using Node js and firebase from ground.',
                price: 5000,
                courses: 34
            },
            {
                img: require('@/assets/img/bundle/react-firebase-cover.png'),
                title: 'Node JS Crash Course',
                content: 'Learn how to make dynamic websites using Node js and firebase from ground.',
                price: 5000,
                courses: 24
            }
        ]
    })

}
</script>

<style scoped>
.bundle {
    max-height: 320px;
    width: 300px !important;
    border: 2px solid #8246B0;
    border-radius: 3px;
}

.bundle_img {
    /* border: 1px solid red; */
    height: 70%;
    overflow: hidden;
}

.bundle_img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.bundle_content {
    border: 1px solid rgb(13, 0, 255);
    height: 30%;
}

.price {
    min-width: 60px;
    min-height: 24px;
    /* color: #8246b09b; */
    background: #DECEEA;
    border: 2px dashed #8246B0;
}

.info {
    min-width: 66px;
    min-height: 24px;
    font-size: 0.9rem;
    /* color: #8246b09b; */
    background: #8246B0 !important;
    color: white !important;
    border-radius: 6px;
    padding: 0.2em 0.3em;
    /* border: 2px dashed #8246B0; */
}
</style>