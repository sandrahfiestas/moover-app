<template>
  <div class="carrusel-container">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-src="../assets/images/slide1.jpg">
        <h1>MOOVER</h1>
      </b-carousel-slide>

      <b-carousel-slide img-src="../assets/images/slide2.jpg">
        <h1>MOOVER</h1>
      </b-carousel-slide>

      <b-carousel-slide img-src="../assets/images/slide3.jpg">
        <h1>MOOVER</h1>
      </b-carousel-slide>

      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="../assets/images/slide4.jpg"
            alt="image slot"
          >
        </template>
        <h1>MOOVER</h1>
      </b-carousel-slide>

      <b-carousel-slide img-src="../assets/images/slide5.jpg">
        <h1>MOOVER</h1>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  data () {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>

<style lang="scss" scoped>
  h1 {
    color: $primary-color;
  }
</style>
