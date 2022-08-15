<template>
  <div class="drawer-menu-comp" @click.self="closeMenu" :class="{ 'hide' : !menuProp}">
    <div class="menu-container">
      <button class="button-close" @click="closeMenu">
        <i class="bi bi-x-lg"></i>
      </button>
      <div class="row">
        <div class="col">
          <div class="menu-content">
            <a href="#">Inicio</a>
            <a href="#">Acerca de</a>
            <a href="#">Servicios</a>
            <a href="#">Contacto</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DrawerMenuComp',
  props: {
    menu: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    menuProp: {
      get() {
        return this.menu;
      },
      set(value) {
        this.$emit('updateMenu', value);
      }
    }
  },
  methods: {
    closeMenu() {
      this.menuProp = false;
    }
  }
}
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
    max-width: 768px;
    height: 100%;
    padding: 3rem;
    position: relative;

    .button-close {
      position: absolute;
      top: 1.6rem;
      left: 2rem;
      background-color: var(--color-white);
      width: 36px;
      height: 36px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      i { font-size: 24px;}
      &:hover {
        background-color: #000000;
        color: #ffffff;
        box-shadow: var(--bs-normal);
      }
    }

    .menu-content {
      display: flex;
      flex-direction: column;
      column-gap: 2rem;
    }
  }
}
</style>