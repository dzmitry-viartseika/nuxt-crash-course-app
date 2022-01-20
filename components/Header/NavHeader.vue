<template>
  <a-layout>
    <a-layout-header class="app-header">
      <div class="app-header__logo logo">
        Logo
      </div>
      <nav>
        <app-nav />
      </nav>
    </a-layout-header>
  </a-layout>
</template>

<script>
import AppNav from '../Menu/AppNav.vue';

export default {
  name: "NavHeader",
  components: {
    AppNav,
  }
}
</script>

<style scoped lang="scss">
@import "scss/variables";

  .app-header {
    position: fixed;
    z-index: 1;
    width: 100%;
    height: 50px;
    display: flex;
    align-items: center;
  }

  .logo {
    color: $color-secondary;
  }
</style>
