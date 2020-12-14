<template lang="pug">
  v-row(class="h-100 align-center justify-center message-container" :class="`message-container-${page}`")
    v-col(cols="6")

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-if="page === 1")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Gulat ka no? Pano muna gulat?
          p Pagpasensyahan mo na yung concept and yung design. Mahina talaga ako don. Huhu
        v-card-actions(class="justify-end")
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 2")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p I just wanna say...
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 3")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Happy anniversary!
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 4")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p I love you from the bottom of my heart. May mga rough days man tayo, pero hindi nababawasan yung pagmamahal ko para sayo.
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 5")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Thank you. Kasi dahil sayo, I have improved a lot.
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 6")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Thank you kasi you always make me happy.
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 7")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Thank you kasi you taught me a lot of things.
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 8")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Everyday, I always say to myself, I wanna be with you for the rest of my life.
          p I wanna take care of you for the rest of our lives.
          p I wanna see your face every time I wake up and before I go to sleep.
          p I wanna have you in my life forever.
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-btn(rounded color="yellow darken-1" outlined @click="page++") Next

      v-card(class="mx-auto" max-width="400" color="#26c6da" v-else-if="page === 9")
        v-img(class="white--text align-end" height="200px" :src="require(`@/assets/images/message/${page}.jpeg`)")
          template(v-slot:placeholder)
              v-row(class="fill-height ma-0" align="center" justify="center")
                v-progress-circular(indeterminate color="blue")
        v-card-text(class="white--text custom--font")
          p Again. Happy 1st anniversary my dear.
        v-card-actions(class="justify-end")
          v-btn(rounded color="indigo darken-1" outlined @click="page--") Back
          v-dialog(v-model="dialog" width="500")
            template(v-slot:activator="{ on, attrs }")
              v-btn(rounded color="yellow darken-1" outlined v-bind="attrs" v-on="on" colorred lighten-2 class="ml-2") Done
            v-card(class="mx-auto" max-width="400" color="#26c6da")
              v-img(class="white--text align-end" height="200px" :src="require('@/assets/images/message/modal.jpeg')")
                template(v-slot:placeholder)
                  v-row(class="fill-height ma-0" align="center" justify="center")
                    v-progress-circular(indeterminate color="blue")
              v-card-text(class="white--text custom--font text-center pt-3")
                .modal-text
                  p.mb-0 I LOVE YOU
                  p.mb-0 AND
                  p.mb-0 I ALWAYS WILL !
              v-card-actions(class="justify-end")
                v-dialog(v-model="catDialog" fullscreen hide-overlay transition="dialog-bottom-transition")
                  template(v-slot:activator="{ on, attrs }")
                    v-btn(rounded color="indigo darken-1" outlined v-bind="attrs" v-on="on" @click="catDialog = true") DO NOT CLICK THIS.
                  custom-modal-bg
                  v-btn(color="red lighten-1" @click="catDialog = false") Close
</template>

<style lang="stylus" scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap')

.h-100
  height 100%

.custom--font
  font-family 'Montserrat', sans-serif

.modal-text
  font-weight bold
  font-size 25px
  line-height 1.9

.message-container
  position relative
  &::before
    position absolute
    content ''
    width 100%
    height 100%
    opacity 0.4
    background-size cover !important
  &-1::before
    background url('~assets/images/bg/1.jpeg') no-repeat center center
  &-2::before
    background url('~assets/images/bg/2.jpeg') no-repeat center center
  &-3::before
    background url('~assets/images/bg/3.jpeg') no-repeat center center
  &-4::before
    background url('~assets/images/bg/4.jpeg') no-repeat center center
  &-5::before
    background url('~assets/images/bg/5.jpeg') no-repeat center center
  &-6::before
    background url('~assets/images/bg/6.jpeg') no-repeat center center
  &-7::before
    background url('~assets/images/bg/7.jpeg') no-repeat center center
  &-8::before
    background url('~assets/images/bg/8.jpeg') no-repeat center center
  &-9::before
    background url('~assets/images/bg/9.jpeg') no-repeat center center
</style>

<script>
export default {
  components: {
    CustomModalBg: () => import('@/components/modal-bg')
  },
  data () {
    return {
      page: 1,
      dialog: false,
      catDialog: false
    }
  }
}
</script>
