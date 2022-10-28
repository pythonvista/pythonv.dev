<template>
    <div class="pro_wrap flex flex-col items-center justify-center px-3 py-3">
        <img class="wave" src="@/assets/img/bg.svg" alt="">
        <img class="wavemob" src="@/assets/img/course-bg.svg" alt="">
        <p class="text-lx3 ma-0 font-bold pa-0 text-primary z-1">PythonV Pro</p>
        <p class="ma-0 pa-0 text-base text-center z-1">Access to every single course & added extras for just ₦2000 a month</p>

        <div class=" bundle mt-3 xs:col-span-3 sm:col-span-3 md:col-span-1 lg:col-span-1 flex flex-column  ">
            <div class="bundle_img ">
                <p class="plan  ma-0 pa-0">Python V <span class="text-primary">PRO</span></p>
                <img src="@/assets/remaster.png" alt="">
            </div>
            <div class="bundle_content  w-full flex flex-col">
                <div class="bundle_info flex flex-col justify-center items-center gap-1 pa-1">
                    <p class="ma-0 pa-0 text-caption text-center text-white font-bold">Python V Pro members get free
                        instant access
                        to all premium PythonV courses.</p>
                    <div class="price px-1 flex items-center justify-center">
                        <span class="text-primary">₦2000/month</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'proplan'

}
</script>

<style scoped>
.pro_wrap {
    background: #f9f9f9;
    position: relative;
}

.bundle {
    height: 320px;
    width: 300px !important;
    border: 3px solid #8246B0;
    border-radius: 15px;
    z-index: 1;
    position: relative;
    overflow: hidden;
}

.bundle_img {
    /* border: 1px solid red; */
    height: 70%;
    overflow: hidden;
    /* border: 1px solid red; */
    position: relative;
}

.plan {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(-45deg);
    font-size: 1.3rem;
    font-weight: bold;

}

.bundle_img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.bundle_content {
    background: #2F2F2F;
    height: 30%;
}

.price {
    min-width: 60px;
    min-height: 24px;
    /* color: #8246b09b; */
    background: #DECEEA;
    border: 2px dashed #8246B0;
}


.wave {
    position: absolute;
    /* top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%; */
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.wavemob {
    display: none;
}
@media (max-width: 640px) {
    .wave {
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