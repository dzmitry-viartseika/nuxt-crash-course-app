<template>
  <main class="app-banner">
    <div class="app-banner__container">
      <h1 class="app-banner__title title">
        Find your Fire Extinguisher
      </h1>
      <p class="app-banner__snippet">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
        Iste iusto illum quidem asperiores, cum nisi aperiam eius ipsa sapiente odit!
      </p>
      <button-default
        text="Start Looking"
      />
    </div>
    <div class="app-banner__image">
      <img src="../../assets/svg/fire-extinguisher.svg" alt="fire extinguisher">
    </div>
  </main>
</template>

<script>
import ButtonDefault from '../Elements/Button/ButtonDefault.vue';

export default {
  name: 'Banner',
  components: {
    ButtonDefault,
  }
}
</script>

<style scoped lang="scss">
@import "assets/scss/variables";

  .app-banner {
    display: flex;
    justify-content: center;
    padding-top: 60px;
    padding-bottom: 40px;
    position: relative;

    &__snippet {
      color: $color-description;
      font-size: 1.25rem;
    }

    &__image {
      width: 27.5rem;
      margin-top: 2rem;
    }
  }

  .title {
    font-weight: 900;
    font-size: 5rem;
  }
</style>
