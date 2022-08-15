<template>
  <div class="home px-5 px-sm-0">
    <HeaderComp />
    <AboutComp />
  </div>
</template>

<script>
import HeaderComp from '@/components/home_view/HeaderComp.vue'
import AboutComp from '@/components/home_view/AboutComp.vue'
export default {
  name: 'HomeView',
  components: {
    HeaderComp,
    AboutComp
  },
}
</script>

<style lang="scss" scoped>
.home {
  padding-top: 78px;
}
</style>
