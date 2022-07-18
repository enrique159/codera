<template>
  <div class="container-fluid">
    <div class="app-bar">
      <div class="app-bar__logo">
        <router-link to="/">
          <img src="@/assets/img/logo-full.svg" alt="logo">
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'AppBarComp',
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

<style lang="scss" scoped>
.app-bar {
  padding: 3rem 2rem 1rem;
  display: flex;

  .app-bar__logo {
    transition: var(--transition-normal);
    &:hover {
      transform: translateY(0.2rem);
    }
  }
}
</style>