<template>
  <div class="container-fluid px-0">
    <div class="app-bar" :class="{ onScroll: !view.topOfPage, 'nav-active': menu }">
      <div class="app-bar__logo">
        <router-link to="/">
          <img src="@/assets/img/logo-full.svg" alt="logo">
        </router-link>
      </div>

      <button class="button-menu" @click="openMenu">
        <i class="bi bi-three-dots"></i>
      </button>
    </div>
    <DrawerMenuComp :menu="menu" v-on:updateMenu="menu = $event"/>
  </div>
</template>

<script>
import DrawerMenuComp from '@/components/DrawerMenuComp.vue'
  export default {
    name: 'AppBarComp',
    components: {
      DrawerMenuComp
    },
    data() {
      return {
        active: 0,
        menu: false,
        view: {
          topOfPage: true,
        },
      }
    },
    beforeMount() {
      window.addEventListener("scroll", this.handleScroll);
    },
    methods: {
      handleScroll() {
        if (window.pageYOffset > 0) {
          if (this.view.topOfPage) this.view.topOfPage = false;
        } else {
          if (!this.view.topOfPage) this.view.topOfPage = true;
        }
      },
      openMenu() {
        this.menu = true;
      },
    },
    beforeDestroy() {
      window.removeEventListener("scroll", this.handleScroll);
    },
  }
</script>

<style lang="scss" scoped>
.app-bar {
  width: 100%;
  height: fit-content;
  padding: 3rem 3rem 3rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  background-color: transparent;
  transition: var(--transition-fast);
  z-index: 10;

  &.onScroll {
    box-shadow: 0 8px 32px 0 rgba(138, 139, 146, 0.158);
    background-color: var(--color-background);
  }

  .app-bar__logo {
    transition: var(--transition-normal);
    &:hover {
      transform: translateY(-0.1rem);
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
        transform: translateY(-0.1rem);
      }
    }
  }

  .button-menu {
    background-color: var(--color-background);
    width: 36px;
    height: 36px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    i { font-size: 24px;}
    &:hover {
      box-shadow: var(--bs-normal);
    }
  }
}
</style>