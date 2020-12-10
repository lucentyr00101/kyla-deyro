<template lang="pug">
  div
    home-parallax(:image="require('@/assets/images/para-1.jpeg')" buttonText="Scroll Down" color="white" height="750")
    image-with-caption(:image="require('@/assets/images/received_449561819078494.jpeg')" caption="Hello. Tignan mo oh ang cute cute mo dito.")
    home-parallax(:image="require('@/assets/images/para-2.jpeg')" buttonText="Eto na game na talaga. Scroll ka na ulit." color="white" height="600")
    image-with-caption(:image="require('@/assets/images/received_574882183257017.jpeg')" caption="")
</template>

<script>
export default {
  components: {
    ImageWithCaption: () => import('@/components/image-with-caption'),
    HomeParallax: () => import('@/components/home-parallax')
  }
}
</script>
