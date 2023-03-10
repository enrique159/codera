<template>
  <div
    class="drawer-menu-comp"
    @click.self="closeMenu"
    :class="{ hide: !menuProp }"
  >
    <div class="menu-container">
      <div class="row justify-content-end">
        <button class="button-close" @click="closeMenu">
          <i class="bi bi-x-lg"></i>
        </button>
      </div>
      <div class="menu-navigation">
        <div class="menu-nav">
          <a href="#">Inicio</a>
          <a href="#">Acerca de</a>
          <a href="#">Servicios</a>
          <a href="#">Portafolio</a>
          <a href="#">Contacto</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DrawerMenuComp",
  props: {
    menu: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    menuProp: {
      get() {
        return this.menu;
      },
      set(value) {
        this.$emit("updateMenu", value);
      },
    },
  },
  methods: {
    closeMenu() {
      this.menuProp = false;
    },
  },
};
</script>

<style lang="scss" scoped>
.drawer-menu-comp {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  right: 0;
  z-index: 11;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  transition: var(--transition-rapida);

  &.hide {
    right: -100%;
  }

  .menu-container {
    background-color: var(--color-white);
    width: 100%;
    max-width: 480px;
    height: 100%;
    padding: 3rem;
    position: relative;

    .button-close {
      background-color: var(--color-white);
      width: 36px;
      height: 36px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      i {
        font-size: 24px;
      }
      &:hover {
        background-color: #000000;
        color: #ffffff;
        box-shadow: var(--bs-normal);
      }
    }

    .menu-navigation {
      width: 100%;
      height: 100%;
      display: grid;
      place-items: center;
    }

    .menu-nav {
      display: flex;
      flex-direction: column;
      row-gap: 1rem;
      height: 100%;
      justify-content: center;
      a {
        text-decoration: none;
      }
    }

    .menu-nav {
      a {
        font-size: 3rem;
        font-weight: 600;
        color: var(--color-black);
        line-height: 1;
        transition: 0.3s ease-in-out;
      }

      a {
        background: linear-gradient(0deg, #231f20, #231f20) no-repeat right
          bottom / 0 var(--bg-h);
        transition: background-size 350ms;
        padding: 0.3rem 1rem 0.6rem 2rem;
        border-radius: 2rem;
        --bg-h: 100%;
      }

      a:where(:hover, :focus-visible) {
        background-size: 100% var(--bg-h);
        background-position-x: left;
        color: var(--color-white);
      }
    }
  }
}
</style>
