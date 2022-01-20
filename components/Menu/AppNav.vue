<template>
  <a-menu
    theme="dark"
    mode="horizontal"
  >
    <a-menu-item
      v-for="item in navigation"
      :key="item.id"
      @click="proceedTo(item.route)"
    >
      {{ item.name }}
    </a-menu-item>
  </a-menu>
</template>

<script>
export default {
  name: 'AppNav',
  props: {
    navigation: {
      type: Array,
      required: true,
    },
  },
  methods: {
    proceedTo(route) {
      if (!route) {
        return //
      }
      this.$router.push(route);
    }
  }
}
</script>

<style scoped>

</style>
