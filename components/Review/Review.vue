<template>
  <div class="app-reviews">
    <h3>Customer Reviews</h3>
    <div v-if="reviewers.results">
      <ReviewCard
        v-for="reviewer in reviewers.results"
        :key="reviewer.login.uuid"
        :review="reviewer"
      />
    </div>
  </div>
</template>

<script>
import ReviewCard from '../../components/Review/ReviewCard.vue';

export default {
  components: {
    ReviewCard,
  },
  data(){
    return {
      reviewers: []
    }
  },
  async fetch() {
    try {
      this.reviewers = await fetch('https://randomuser.me/api/?results=5').then((res) => res.json())
    } catch (e) {
      console.error(e);
    }
  }
}
</script>

<style lang="scss" scoped>
 .app-reviews {
   padding-bottom: 50px;
 }
</style>
