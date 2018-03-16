<template>
  <div class="container__g">
    <carousel>
      <carousel-slide v-for="n in slides">
        <div class="text">
          Slide {{ n }}
        </div>
        <img :src="'http://lorempicsum.com/rio/630/300/' + n" />
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
      slides: 5
    }
  },
  methods: {
  },
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
    width: 100vw;
    height: 100vh;
    position: relative;
    display: grid;
    justify-content: center;
  }
  .text {
    position: absolute;
    top: 33vh;
    left: 41vw;
    color: white;
    font-size: 7em;
    font-family: sans-serif;
  }
  img {
    width: 100%;
  }
</style>
