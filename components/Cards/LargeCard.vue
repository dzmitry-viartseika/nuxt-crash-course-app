<template>
  <nuxt-link :to="`/products/${card.id}`" class="app-card">
    <img class="app-card__image" :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" alt="">
    <h3 class="app-card__title title">{{ card.title }}</h3>
    <p class="app-card__snippet">
      {{card.snippet }}
    </p>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped lang="scss">
@import './assets/scss/variables';

.app-card {
  width: 31.5%;
  height: 25rem;
  border: none;
  padding: 0;
  cursor: pointer;

  &__snippet {
    color: $color-description;
  }

  &__image {
     height: 65%;
     border-radius: 0.5rem;
   }
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.title {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
</style>
