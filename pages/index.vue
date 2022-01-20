<template>
  <div class="app__container">
    <Banner />
    <LargeCardDisplay
      v-for="cardInfoLarge in largeCardInfo"
      :key="cardInfoLarge.id"
      :cardsSection="cardInfoLarge"
    />
    <SmallCardDisplay
      v-for="cardInfoSmall in smallCardSections"
      :key="cardInfoSmall.id"
      :cardsSection="cardInfoSmall"
    />
  </div>
</template>

<script>
import Banner from '../components/Banner/Banner.vue';
import LargeCardDisplay from '../components/Cards/LargeCardDisplay.vue';
import SmallCardDisplay from '../components/Cards/SmallCardDisplay.vue';
import largeCardSections from '../constants/largeCardSections';
import smallCardSections from '../constants/smallCardSections';

export default {
  name: 'IndexPage',
  components: {
    Banner,
    LargeCardDisplay,
    SmallCardDisplay,
  },
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections,
    }
  }
}
</script>

<style lang="scss">
.app__container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
