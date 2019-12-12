<template>
  <div>
    <b-navbar
      type="is-primary"
      has-shadow
      wrapper-class="container"
    >
      <template slot="brand">
        <b-navbar-item
          :to="{ path: '/' }"
          tag="router-link"
          class="has-background-light"
        >
          <img
            src="~assets/logo.png"
            alt="TurtleCoin"
          >
        </b-navbar-item>
      </template>

      <template slot="start" />

      <template slot="end">
        <b-navbar-item tag="nuxt-link" to="/services">
          {{ $t('menu.services') }}
        </b-navbar-item>

        <b-navbar-item tag="nuxt-link" to="/about">
          {{ $t('menu.about') }}
        </b-navbar-item>

        <b-navbar-item tag="nuxt-link" to="/contact">
          {{ $t('menu.contact') }}
        </b-navbar-item>
      </template>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  computed: {
    locales () {
      return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale)
    }
  }
}
</script>
