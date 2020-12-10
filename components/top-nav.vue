<template lang="pug">
  v-system-bar(
    dark
    fixed
  )
    v-icon mdi-message
    span 10 unread messages
    v-spacer
    v-icon mdi-wifi-strength-4
    v-icon mdi-singular-cellular-outline
    v-icon mdi-battery
    span {{ time }}
</template>

<script>
import moment from 'moment'

export default {
  data () {
    return {
      time: moment().format('hh:mm:ss A')
    }
  },
  mounted () {
    setInterval(this.setTime, 1000)
  },
  methods: {
    setTime () {
      this.time = moment().format('hh:mm:ss A')
    }
  }
}
</script>
