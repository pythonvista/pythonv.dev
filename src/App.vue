<template>
  <v-app class="app">
    <v-main>
      <router-view />
    </v-main>
    <v-bottom-navigation v-show="nav" class="bottom-nav md:hidden ma-0 pa-0" color="indigo">
      <div class="w-full h-full flex justify-around align-center ma-0 pa-0">
        <v-btn color="transparent" class="flex-1 ">
          <v-icon>mdi-home</v-icon>
        </v-btn>
        <v-btn color="transparent" class="flex-1">
          <v-icon>mdi-account</v-icon>
        </v-btn>
        <v-btn color="transparent" class="flex-1">
          <v-icon>mdi-login</v-icon>
        </v-btn>
        <v-btn color="transparent" class="flex-1">
          <v-icon>mdi-logout</v-icon>
        </v-btn>
      </div>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
import { nav } from "@/main.js";
export default {
  name: 'App',
  
  data: () => ({
    //
    nav:false
  }),
  created() {
    nav.$on("openNav", () => {
      // this.snackcolor = event.color
      // this.snackbar = true;
      // this.snackmsg = event.msg
      this.nav = !this.nav
    });
  },
};
</script>

<style scoped>
.app {
  height: 100vh !important;
  overflow: hidden;
  overflow-y: scroll;
  position: relative;
}

.app::-webkit-scrollbar{
  width: 10px;
  background: #61109e66;
}
.app::-webkit-scrollbar-thumb{
  background: #60109E;
}


.bottom-nav {
  height: 46px !important;
  background: white;
  transition: 0.5s !important;
}

@media (max-width: 640px) {
  .app::-webkit-scrollbar{
  display: none;
}

}
</style>