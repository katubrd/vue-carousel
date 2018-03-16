<template lang="html">
  <transition :name="transition">
    <div v-show="visible" class="container__slide">
      <!-- Index: {{ index }} -->
      <slot></slot>
    </div>
  </transition>
</template>

<script>
  export default {
    data () {
      return {
        index: 0
      }
    },
    computed: {
      transition() {
        if(this.$parent.direction){
          return 'slide-' + this.$parent.direction }
        },
      visible () { return this.index === this.$parent.index }
    }
  }
</script>

<style lang="css">
  .container__slide {
    width: 100%;
  }
  .slide-right-enter-active{
    animation: slideRightIn .5s;
  }

  .slide-right-leave-active {
    animation: slideRightOut .5s;
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    rigth: 0;
    bottom: 0;
  }

  @keyframes slideRightIn {
    from { transform: translateX(100%); }
    to { transform: translateX(0); }
  }

  @keyframes slideRightOut {
    from { transform: translateX(0); }
    to { transform: translateX(-100%); }
  }

  .slide-left-enter-active{
    animation: slideLeftIn .5s;
  }

  .slide-left-leave-active {
    animation: slideLeftOut .5s;
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    rigth: 0;
    bottom: 0;
  }

  @keyframes slideLeftIn {
    from { transform: translateX(-100%); }
    to { transform: translateX(0); }
  }

  @keyframes slideLeftOut {
    from { transform: translateX(0); }
    to { transform: translateX(100%); }
  }










</style>
