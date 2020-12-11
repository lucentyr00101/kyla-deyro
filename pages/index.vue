<template lang="pug">
  div
    home-parallax(:image="require('@/assets/images/para-1.jpeg')" buttonText="Scroll Down" color="white" height="750")
    image-with-caption(:image="require('@/assets/images/received_449561819078494.jpeg')" caption="Hello. Tignan mo oh ang cute cute mo dito.")
    home-parallax(:image="require('@/assets/images/para-2.jpeg')" buttonText="Eto na game na talaga. Scroll ka na ulit." color="white" height="600")
    template(v-for="(item, i) in items")
      v-divider
      image-with-caption(:image="require(`@/assets/images/${item.image}`)" :caption="item.text" :date="item.date")
</template>

<script>
export default {
  components: {
    ImageWithCaption: () => import('@/components/image-with-caption'),
    HomeParallax: () => import('@/components/home-parallax')
  },
  data () {
    return {
      items: [
        { text: 'Eto pa yun yung picture mo non. Huhu. Pagkakita ko palang swipe right agad eh.', image: '42614787_2091410157536289_6231706309058625536_n.jpg' },
        { text: '1 out of 2 ng kaunaunahang pictures natin together. Huhu bat ganito itsura ko.', image: 'IMG_20190812_131130.jpg', date: '2019-08-12' },
        { text: '2 out of 2. Ang happy happy mo naman pu.', image: 'IMG_20190812_131123.jpg', date: '2019-08-12' },
        { text: 'San punta? Bat tulog tulog ang bata? Charot lang. Alam ko otw maginhawa to eh or UP. Hahaha', image: 'IMG_20190817_155507.jpg', date: '2019-08-17' },
        { text: 'Ay oo tama maginhawa nga. Eto kinain natin non.', image: 'IMG_20190817_185540.jpg', date: '2019-08-17' },
        { text: 'Kaya madalas kita kinakain eh. @Glorietta ata to', image: 'IMG_20190825_174947.jpg', date: '2019-08-25' },
        { text: 'Pocky Model #1 @SM Makati I guess?', image: 'IMG_20190913_192219.jpg', date: '2019-09-13' },
        { text: 'Pocky Model #2 @SM Makati I guess?', image: 'IMG_20190913_192220.jpg', date: '2019-09-13' },
        { text: 'Pocky Model #3 @SM Makati I guess?', image: 'IMG_20190913_192221.jpg', date: '2019-09-13' },
        { text: 'Pocky Model #4 @SM Makati I guess?', image: 'IMG_20190913_192224.jpg', date: '2019-09-13' },
        { text: 'Pocky Model #5 @SM Makati I guess?', image: 'IMG_20190913_192225.jpg', date: '2019-09-13' },
        { text: 'Pinagbigyan lang kita nito eh.', image: 'IMG_20190913_194731.jpg', date: '2019-09-13' },
        { text: '@Chowking SM North.', image: 'IMG_20190914_122013.jpg', date: '2019-09-14' },
        { text: 'Ikaw tlaga dahilan kung bakit ako natanggap dito kase I decided to improve myself, lumabas sa comfort zone ko. And I thank you for that.', image: 'IMG_20190927_122416.jpg', date: '2019-09-27' },
        { text: 'Mercato #1 Sino uupakan mo? Bat parang galit ka? :( Sorry na.', image: 'IMG_20190927_191428.jpg', date: '2019-09-27' },
        { text: 'Mercato #2', image: 'IMG_20190927_191432.jpg', date: '2019-09-27' },
        { text: 'Mercato #3', image: 'IMG_20190927_191439.jpg', date: '2019-09-27' }
      ]
    }
  }
}
</script>
