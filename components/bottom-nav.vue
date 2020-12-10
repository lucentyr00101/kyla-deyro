<template lang="pug">
  v-bottom-navigation(
    v-model="value"
    :background-color="color"
    dark
    shift
    grow
  )
    v-btn
      span Home
      v-icon mdi-home
    v-btn
      span Image
      v-icon mdi-folder-multiple-image
    v-btn
      span Message
      v-icon mdi-thought-bubble
</template>

<script>
export default {
  data () {
    return {
      value: 0
    }
  },
  computed: {
    color () {
      switch (this.value) {
        case 0: return 'blue-grey'
        case 1: return 'teal'
        case 2: return 'brown'
        case 3: return 'indigo'
        default: return 'blue-grey'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
.v-btn
  height 100% !important
</style>
