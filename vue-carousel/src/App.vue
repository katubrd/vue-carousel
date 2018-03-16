<template>
  <div class="container__g">
    <carousel>
      <carousel-slide>
        <div class="text">
          Hi! here is the first one!
        </div>
        <img src="./assets/img/watermelon.jpg" />
      </carousel-slide>
      <carousel-slide>
        <div class="text">
          Hi! here is the second one!
        </div>
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
  .text {
    position: absolute;
    top: 33vh;
    left: 41vw;
  }
  img {
    width: 100%;
  }
</style>
