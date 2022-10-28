<template>
  <v-app class="app">
    <v-main>
      <router-view />
    </v-main>
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