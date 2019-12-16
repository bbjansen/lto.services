<template>
  <div>
    <Navigation />

    <section class="main-content">
      <div class="container">
        <nuxt />
      </div>
    </section>

    <Footer />
  </div>
</template>

<script>
import Navigation from '~/components/Navigation'
import Footer from '~/components/Footer'

export default {
  components: {
    Navigation,
    Footer
  }
}
</script>
