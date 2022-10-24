<template>
  <div>
    <HomeNav/>
    <router-view></router-view>
  </div>
</template>

<script>
import HomeNav from '@/components/utility/nav/HomeNav.vue'
  export default {
    name: 'Home',

    components: {
      HomeNav
    },
  }
</script>
<style scoped>

</style>