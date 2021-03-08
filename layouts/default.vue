<template>
  <div>
    <Header />
    <main>
      <Nuxt />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from '../components/Header'
import Footer from '../components/Footer'

export default {
  components: {
    Header,
    Footer
  },
  data: () => {
    return {
      slides: [
        {
          image: 'https://i.ibb.co/Kwpf1LM/Abstract-decorative-blue-wave-banner-design-vector.jpg',
          text: 'Imagen Uno'
        },
        {
          image: 'https://i.ibb.co/jDy4F1t/Abstract-stylish-wave-banner-design-vector.jpg',
          text: 'Imagen Dos'
        },
        {
          image: 'https://i.ibb.co/f9QyPkD/Abstract-pink-color-wave-design-banner-vector.jpg',
          text: 'Imagen Tres'
        }
      ]
    }
  }
}
</script>

<style lang="scss">

</style>
