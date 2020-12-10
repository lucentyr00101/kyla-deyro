<template lang="pug">
  div
    v-parallax(:src="require('@/assets/images/received_416654145648575.jpeg')")
      v-btn(outlined color="white")
        v-icon(left) mdi-chevron-double-down
        | Scroll Down
    v-row(no-gutters)
      v-col(cols="12")
        v-card
          v-img(:src="require('@/assets/images/received_449561819078494.jpeg')")
    v-row(no-gutters)
      v-col(cols="12")
        v-sheet(color="red lighten-3")
          span Hello. Hehe
</template>

<style lang="stylus" scoped>
.v-parallax
  height 96.9vh !important
</style>
