<template>
  <v-app class="app">
    <v-main>
      <router-view />
    </v-main>
    <v-bottom-sheet v-model="nav">
      <v-sheet class="text-center" height="40vh">
        <div class="nav_wrap" >
          <v-list dense rounded>
            <v-list-item v-for="item in items" :key="item.title" link>


              <v-list-item-content>
                <v-list-item-title  class="text-primary">{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>

          <v-btn outlined color="#8246B0" class="nav-btn">GET STARTED</v-btn>
        </div>



      </v-sheet>
    </v-bottom-sheet>
  </v-app>
</template>

<script>
import { nav } from "@/main.js";
export default {
  name: 'App',

  data: () => ({
    items: [
    { title: 'Home', icon: 'mdi-view-dashboard' },
      { title: 'Courses', icon: 'mdi-view-dashboard' },
      { title: 'Degree & Specification', icon: 'mdi-forum' },
      { title: 'Cohorts & Schools', icon: 'mdi-forum' },
      { title: 'PythonV Pro', icon: 'mdi-forum' },
    ],
    nav: false
  }),
  created() {
    nav.$on("openNav", () => {
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

.app::-webkit-scrollbar {
  width: 10px;
  background: #61109e66;
}

.app::-webkit-scrollbar-thumb {
  background: #60109E;
}


.bottom-nav {
  height: 46px !important;
  background: white;
  transition: 0.5s !important;
}

.nav_wrap{
  position: relative;
  height: 100%;
  padding: .3em 0;
}

.nav-btn{
  position: absolute;
  bottom: 5px;
  left: 50%;
  transform: translate(-50%, 0);
  width: 95%;
}

@media (max-width: 640px) {
  .app::-webkit-scrollbar {
    display: none;
  }

}
</style>