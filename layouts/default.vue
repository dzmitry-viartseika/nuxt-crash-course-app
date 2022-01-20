<template>
  <div>
    <nav-header />
    <nuxt />
    <app-footer />
  </div>
</template>

<script>
import NavHeader from '../components/Header/NavHeader.vue';
import AppFooter from '../components/Footer/AppFooter.vue';

export default {
  name: "default",
  components: {
    NavHeader,
    AppFooter,
  }
}
</script>

<style scoped>

</style>
