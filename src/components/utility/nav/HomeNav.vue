<template>
    <v-app-bar app light style="width:100% !imporatnt"
        class="nav px-2 elevation-0 border-bottoms flex justify-between items-center bg-white ">
        <div class="nav-wrap flex sm:justify-evenly items-center align-center w-full md:justify-evenly lg:justify-evenly">

            <div class=" h-full flex w-full py-2 justify-start align-center logo">
                <img class="w-10"  src="@/assets/img/logo.png">
            </div>

            <div data-aos="fade-down" class=" w-full hidden sm:hidden md:flex md:justify-center gap-4  md:items-center nav-link">
                <router-link :to="{name: 'courses'}"><p class="text-primary ma-0 text-base font-bold">Courses</p></router-link>
                <router-link :to="{name: 'courses'}"><p class="text-primary ma-0 text-base font-bold">Design & Specification</p></router-link>
                <router-link :to="{name: 'courses'}"><p class="text-primary ma-0 text-base font-bold">School & Cohorts</p></router-link>
            </div>
            <div class="w-full hidden sm:hidden md:flex md:justify-end auth">
                <v-btn x-small depressed color="#60109E" class="btn_hover">
                    <p class="ma-0 pa-0 ">Get Started</p>
                   
                </v-btn>
            </div>
            <div class="flex w-full sm:justify-end md:hidden  justify-end md:justify-end align-center auth">
                <v-btn @click="openNav" small fab depressed color="deep-purple" outlined>
                    <v-icon>mdi-menu</v-icon>
                    <!-- <img src="@/assets/logo.png" alt=""> -->
                </v-btn>

            </div>

        </div>


    </v-app-bar>
</template>

<script>
import { nav } from "@/main.js";
export default {
    name: 'HomeNav',
    methods: {
        openNav() {
            nav.$emit("openNav");
        },
    }

}
</script>

<style scoped>
.nav {
    background-color: white !important;
    /* min-height: 12vh !important; */
    overflow: hidden;

}

v-toolbar__content{
    height: 100% !important;
}

.nav-wrap{
    height: 100%;
    width: 100% !important;
}

.logo {
    flex: 1;
}

.nav-link {
    flex: 3;
}

.auth {
    flex: 1;
}
</style>