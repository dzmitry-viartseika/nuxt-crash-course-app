<template>
  <div>
    <Banner />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardSections"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
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
