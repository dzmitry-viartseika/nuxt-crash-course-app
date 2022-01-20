<template>
  <div class="container">
    <item
      v-for="rental in myRentals"
      :key="rental.id"
      :item="rental"
    />
  </div>
</template>

<script>
import { mapState } from 'vuex';
import Item from '../components/Item/Item';
export default {
  layout: 'no-navigation',
  components: {
    Item,
  },
  computed: {
    ...mapState([
      'myRentals'
    ])
  }
}
</script>

<style scoped>
.container {
  padding: 5rem 0;
}
</style>
