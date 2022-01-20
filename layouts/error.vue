<template>
  <div class="app-page">
    <h1>Page not Founded 404</h1>
    <button-default
      text="Back to Home Page"
      @handleClick="handleClick"
    />
  </div>
</template>

<script>
import ButtonDefault from '../components/Elements/Button/ButtonDefault.vue';

export default {
  components: {
    ButtonDefault,
  },
  name: "error",
  methods: {
    handleClick() {
      console.log('proceedToHome')
      this.$router.push('/');
    }
  }
}
</script>

<style scoped lang="scss">
  .app-page {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
</style>
