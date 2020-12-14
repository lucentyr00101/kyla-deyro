<template lang="pug">
  v-bottom-navigation(
    v-model="value"
    :background-color="color"
    dark
    shift
    grow
    fixed
  )
    v-btn
      span Home
      v-icon mdi-home
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
  },
  watch: {
    value () {
      switch (this.value) {
        case 0:
          this.$router.push({ name: 'index' })
          break
        case 1:
          this.$router.push({ name: 'gallery' })
          break
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
.v-btn
  height 100% !important
</style>
