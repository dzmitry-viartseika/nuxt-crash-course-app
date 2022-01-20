<template>
  <div class="app-products">
    <div class="app__container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0,1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import largeCardSections from '../../constants/largeCardSections';
import smallCardSections from '../../constants/smallCardSections';
import LargeCardDisplay from "../../components/Cards/LargeCardDisplay";
import SmallCardDisplay from "../../components/Cards/SmallCardDisplay";

export default {
  components: {
    LargeCardDisplay,
    SmallCardDisplay,
  },
  data(){
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    }
  }
}
</script>

<style scoped lang="scss">
.app-products {
  padding-top: 60px;
}
</style>
