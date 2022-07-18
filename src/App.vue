<template>
  <div id="app">
    <AppBarComp></AppBarComp>
    <router-view/>
  </div>
</template>

<script>
import AppBarComp from './components/AppBarComp.vue'
export default {
  name: 'App',
  components: {
    AppBarComp
  },
  data() {
    return {
      //
    }
  },
  methods: {
    //
  }
}
</script>
<style lang="scss">
@import '@/assets/fonts.css';
@import '@/assets/styles.scss';
</style>
