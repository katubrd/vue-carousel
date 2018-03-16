<template>
  <div class="container__g">
    <carousel>
      <carousel-slide>
        Hi! here is the first one!
        <img src="./assets/img/watermelon.jpg" />
      </carousel-slide>
      <carousel-slide>
        Hi! here is the second one!
        <img src="./assets/img/palms.jpg" />
      </carousel-slide>
    </carousel>
  </div>
</template>

<script>
import Carousel from './components/carousel/carousel'
import CarouselSlide from './components/carousel/carouselSlide'

export default {
  name: 'app',
  data () {
    return {
    }
  },
  methods: {},
  components: {
    Carousel,
    CarouselSlide
  }
}
</script>

<style lang="scss">
  body {
    margin: 0;
    padding: 0;
  }
  .container__g {
    width: 100%;
    height: 100vh;
    position: relative;
    display: grid;
    justify-content: center;
  }

  img {
    width: 100%;
  }
</style>
