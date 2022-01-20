<template>
  <div class="container">
    <h3 class="header">{{ cardsSection.title }}</h3>
    <div class="card-container">
      <small-card
        v-for="card in cardsSection.cards"
        :key="card.id"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
import SmallCard from "./SmallCard";

export default {
  props: ["cardsSection"],
  components: {
    SmallCard,
  }
}
</script>

<style scoped>
.container {
  padding: 2rem 0
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}
.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
