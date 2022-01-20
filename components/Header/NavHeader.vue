<template>
  <a-layout>
    <a-layout-header class="app-header">
      <div
        class="app-header__logo logo"
        @click="proceedToHome"
      >
        Logo
      </div>
      <nav>
        <app-nav :navigation="navigation"/>
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
  },
  props: {
    navigation: {
      type: Array,
      required: true,
    },
  },
  methods: {
    proceedToHome() {
      if (this.$route.path !== '/') {
        this.$router.push('/');
      }
      return //
    }
  }
}
</script>

<style scoped lang="scss">
@import "assets/scss/variables";

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
