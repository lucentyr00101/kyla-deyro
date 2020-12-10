<template lang="pug">
  v-parallax(:src="image" :height="height")
    v-btn(:outlined="outlined" :color="color")
      v-icon(left) mdi-chevron-double-down
      | {{ buttonText }}
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      default: ''
    },
    buttonText: {
      type: String,
      default: ''
    },
    color: {
      type: String,
      default: ''
    },
    height: {
      type: String,
      default: '500'
    },
    outlined: {
      type: Boolean,
      default: false
    }
  }
}
</script>
