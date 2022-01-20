<template>
  <a-button :type="type">
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
  }
}
</script>

<style scoped>

</style>
