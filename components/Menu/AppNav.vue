<template>
  <a-menu
    theme="dark"
    mode="horizontal"
    :default-selected-keys="['2']"
  >
    <a-menu-item key="1">
      nav 1
    </a-menu-item>
    <a-menu-item key="2">
      nav 2
    </a-menu-item>
    <a-menu-item key="3">
      nav 3
    </a-menu-item>
  </a-menu>
</template>

<script>
export default {
  name: "AppNav"
}
</script>

<style scoped>

</style>
