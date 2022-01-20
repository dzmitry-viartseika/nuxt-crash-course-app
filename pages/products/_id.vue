<template>
  <div class="app-product">
    <div v-if="product" class="app__container">
      <div class="app-product-container">
        <img :src="require(`@/assets/images/${product.image}`)" alt="" class="image">
        <div class="info-box">
          <h1>{{ product.title }}</h1>
          <p class="snippet">{{ product.snippet }}</p>
          <RentModal
            :product="product"
          />
        </div>
      </div>
      <div class="app-product-includes">
        <div class="app-product-includes__item">
          <h6>Super Effective</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
        </div>
        <div class="app-product-includes__item">
          <h6>Clean & Tidy</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
        </div>
        <div class="app-product-includes__item">
          <h6>Cancel Anytime</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
        </div>
        <div class="app-product-includes__item">
          <h6>Satisfaction Guaranteed</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
        </div>
      </div>
      <div class="description-container">
        <p>
          {{ product.description }}
        </p>
      </div>
      <Reviews />
    </div>
    <div v-else class="container padding">
      <PageNotFound />
    </div>
  </div>
</template>

<script>
import RentModal from '../../components/Modals/RentModal/RentModal.vue';
import Reviews from '../../components/Review/Review.vue';
import PageNotFound from '../../components/Placeholders/PageNotFound.vue';

export default {
  components: {
    RentModal,
    Reviews,
    PageNotFound,
  },
  computed: {
    product() {
      return this.$store.getters.getProductById(this.$route.params.id);
    }
  }
}
</script>

<style scoped lang="scss">
@import './assets/scss/variables';

.app-product {
  padding-top: 60px;

  &-container {
    display: flex;
    justify-content: space-between;
  }

  &-includes {
    padding-top: 20px;
    padding-bottom: 20px;

    &__item {

      h6 {
        font-size: 14px;
        font-weight: bold;
      }
    }
  }
}

.image {
  width: 59%;
  height: 25rem;
}
.info-box {
  width: 39%;
  background-color: rgba($color-description, .2);
  padding: 1rem;
  border-radius: 0.5rem;
}
.whats-included-container {
  border-bottom: 0.1rem solid rgba($color-description, .2);
}

.included-container {
  margin-top: 1.5rem;
}

</style>
