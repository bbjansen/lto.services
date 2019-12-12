<template>
  <div>
    <b-navbar
      type=""
      has-shadow
      wrapper-class="container"
    >
      <template slot="brand">
        <b-navbar-item
          :to="{ path: '/' }"
          tag="router-link"
          class="has-background-light has-text-grey-dark is-size-3 has-text-weight-bold"
        >
          <img
            src="~assets/logo.png"
            alt="LTO Services"
            height="28"
          >
          LTO Services
        </b-navbar-item>
      </template>

      <template slot="start" />

      <template slot="end">
        <b-navbar-item
          :to="{ path: '/pool' }"
          tag="router-link"
          class="has-text-grey-dark is-size-5 has-text-weight-bold"
        >
          Lease
        </b-navbar-item>
        <b-navbar-item
          :to="{ path: '/projects' }"
          tag="router-link"
          class="has-text-grey-dark is-size-5 has-text-weight-bold"
        >
          Projects
        </b-navbar-item>
        <b-navbar-dropdown
          :value="this.$i18n.locale"
          :label="$t('language')"
          hoverable

          class="has-text-grey-dark is-size-5 has-text-weight-bold"
        >
          <b-navbar-item
            v-for="locale of locales"
            :key="locale.code"
            :to="switchLocalePath(locale.code)"
            :value="locale.code"
            tag="nuxt-link"
          >
            {{ locale.name }}
          </b-navbar-item>
        </b-navbar-dropdown>
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
