<template>
  <div>
    <nav-header :navigation="navigation"/>
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
  },
  data: () => ({
    navigation: [
      {
        id: 1,
        name: 'Products',
        route: '/products'
      },
      {
        id: 2,
        name: 'My Items',
        route: '/my-items'
      },
    ]
  })
}
</script>

<style scoped lang="scss">

</style>
