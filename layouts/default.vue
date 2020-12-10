<template lang="pug">
  v-app
    v-main
      Nuxt
    v-footer(app padless)
      bottom-nav
</template>

<script>
export default {
  components: {
    BottomNav: () => import('@/components/bottom-nav')
  }
}
</script>
