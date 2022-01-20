<template>
  <a-button
    :type="type"
    @click="handleClick"
  >
    {{ text }}
  </a-button>
</template>

<script>
export default {
  name: "ButtonDefault",
  props: {
    text: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      default: 'primary',
    }
  },
  methods: {
    handleClick() {
      this.$emit('handleClick');
    }
  }
}
</script>

<style scoped>

</style>
