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
                p.text-caption.mb-1.font-italic Date Taken: {{ transformDate(date) }} ({{ transformDateFromNow(date) }})
                span.text-body-2 {{ caption }}
</template>

<script>
import moment from 'moment'

export default {
  props: {
    caption: {
      type: String,
      default: ''
    },
    image: {
      type: String,
      default: ''
    },
    date: {
      type: String,
      default: 'unknown'
    }
  },
  methods: {
    transformDate (date) {
      if (date === 'unknown') {
        return 'idk'
      } else {
        return moment(date).format('MMM DD YYYY')
      }
    },
    transformDateFromNow (date) {
      if (date === 'unknown') {
        return 'idk also'
      } else {
        return moment(date).fromNow()
      }
    }
  }
}
</script>
