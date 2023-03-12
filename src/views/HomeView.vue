<template>
  <div class="home px-2 px-sm-0">
    <HeaderComp />
    <AboutComp />
    <ServicesComp />
    <Portfolio />
    <ContactComp />
    <FooterComp />
  </div>
</template>

<script>
import HeaderComp from '@/components/home_view/HeaderComp.vue'
import AboutComp from '@/components/home_view/AboutComp.vue'
import ServicesComp from '@/components/home_view/ServicesComp.vue'
import Portfolio from '@/components/home_view/PortfolioComp.vue'
import ContactComp from '@/components/home_view/ContactComp.vue'
import FooterComp from '@/components/FooterComp.vue' 
export default {
  name: 'HomeView',
  components: {
    HeaderComp,
    AboutComp,
    ServicesComp,
    Portfolio,
    ContactComp,
    FooterComp
  },
}
</script>

<style lang="scss" scoped>
.home {
  padding-top: 78px;
}
</style>
