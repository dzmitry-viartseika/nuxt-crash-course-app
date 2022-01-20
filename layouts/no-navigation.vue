<template>
  <div class="app-cart">
      <div class="app__container">
        <NuxtLink to="/">
          Go Back
        </NuxtLink>
        <Nuxt />
      </div>
  </div>
</template>

<script>
export default {
  name: "no-navigation"
}
</script>

<style scoped lang="scss">
  .app-cart {
    padding-top: 60px;
  }
</style>
