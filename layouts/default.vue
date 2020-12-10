<template lang="pug">
  v-app
    top-bar
    v-main
      Nuxt
    v-footer(padless)
      bottom-nav
</template>

<script>
export default {
  components: {
    BottomNav: () => import('@/components/bottom-nav'),
    TopBar: () => import('@/components/top-nav')
  }
}
</script>
