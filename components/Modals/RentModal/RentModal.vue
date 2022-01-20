<template>
  <div>

    <button-default
      text="Rent"
      @handleClick="showModal"
    />

    <a-modal
      v-model="visible"
      title="Basic Modal"
      @ok="handleOk"
    >
      <vc-date-picker
        :value="null"
        color="indigo"
        is-dark
        is-range
      />
      <div class="calendar-container">
        <div class="text-container">
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Asperiores quis soluta quia neque! Ea modi, a omnis eligendi enim ducimus asperiores. Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, autem?</p>
        </div>
      </div>

      <button-default
        text="Order"
        @handleClick="order"
      />
    </a-modal>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
import ButtonDefault from '../../Elements/Button/ButtonDefault.vue';

export default {
  components: {
    ButtonDefault,
  },
  props: {
    product: {
      type: Object,
      required: true,
    }
  },
  data() {
    return {
      visible: false,
      selectedDate: null,
      days: [],
    };
  },
  methods: {
    showModal() {
      this.visible = true;
    },
    handleOk(e) {
      this.visible = false;
    },
    ...mapMutations(['addItem']),
    order() {
      this.addItem(this.product.id);
      this.visible = false;
    },
  }
}
</script>


<style scoped lang="scss">

</style>
