<template>
  <div>
    <Navigation />
    <section class="main-content">
      <div class="container">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
import Navigation from '~/components/Navigation'

export default {
  components: {
    Navigation
  }
}
</script>
