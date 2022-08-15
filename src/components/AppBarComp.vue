<template>
  <div class="container-fluid">
    <div class="app-bar">
      <div class="app-bar__logo">
        <router-link to="/">
          <img src="@/assets/img/logo-full.svg" alt="logo">
        </router-link>
      </div>

      <div class="app-bar__menu">
        <a href="#home">Inicio</a>
        <a href="#about">Acerca de</a>
        <a href="#services">Servicios</a>
        <a href="#contact">Contacto</a>
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
  justify-content: space-between;
  align-items: center;

  .app-bar__logo {
    transition: var(--transition-normal);
    &:hover {
      transform: translateY(0.2rem);
    }
  }

  .app-bar__menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: var(--transition-normal);
    column-gap: 2rem;

    a {
      text-decoration: none;
      font-size: 1.2rem;
      font-weight: var(--font-medium);
      color: var(--color-text-dark);
      transition: var(--transition-normal);
      &:hover {
        transform: translateY(0.2rem);
      }
    }
  }
}
</style>