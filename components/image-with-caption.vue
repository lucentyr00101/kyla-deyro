<template lang="pug">
  div
    v-row(no-gutters)
      v-col(cols="12")
        v-card
          v-img(:src="image")
    v-row(no-gutters)
      v-col(cols="12")
        v-sheet(color="blue lighten-3")
          v-container(fluid)
            v-row
              v-col.text-center(cols="12")
                span {{ caption }}
</template>

<script>
export default {
  props: {
    caption: {
      type: String,
      default: ''
    },
    image: {
      type: String,
      default: ''
    }
  }
}
</script>
