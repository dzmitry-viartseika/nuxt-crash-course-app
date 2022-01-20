<template>
  <div class="app-review-card">
    <div class="app__container">
      <div class="app-review-card__photo">
        <img :src="review.picture.large" alt="">
      </div>
    </div>
    <div class="text-container" >
      <h6>{{review.login.username}}</h6>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellendus quam magni beatae possimus debitis.</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    review: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped lang="scss">
  .app-review-card {
    margin-top: 1.5rem;
    height: 4rem;
    display: flex;

    &__photo img {
      width: 4rem;
      height: 4rem;
      border-radius: 100%;
    }
  }
</style>
