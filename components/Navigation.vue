<template>
  <div>
    <b-navbar
      type="is-light"
      has-shadow
      wrapper-class="container"
    >
      <template slot="brand">
        <b-navbar-item
          :to="{ path: '/' }"
          tag="router-link"
        >
          <b-icon
            icon="call-merge"
            size="is-large"
            type="is-primary"
            style="padding-right: 10px"
          />
          <p class="has-text-grey-dark is-size-3 has-text-weight-bold">
            LTO Services
          </p>
        </b-navbar-item>
      </template>

      <template slot="start" />

      <template slot="end">
        <b-navbar-item
          tag="a"
          href="https://lease.lto.services"
          class="has-text-primary is-size-5 has-text-weight-bold"
        >
          {{ $t('menu.lease') }}
        </b-navbar-item>
        <b-navbar-item
          :to="{ path: '/' }"
          tag="router-link"
          class="has-text-grey-dark is-size-5 has-text-weight-bold"
        >
          {{ $t('menu.services') }}
        </b-navbar-item>
        <b-navbar-item
          :to="{ path: '/projects' }"
          tag="router-link"
          class="has-text-grey-dark is-size-5 has-text-weight-bold"
        >
          {{ $t('menu.projects') }}
        </b-navbar-item>
        <b-navbar-item
          :to="{ path: '/blog' }"
          tag="router-link"
          class="has-text-grey-dark is-size-5 has-text-weight-bold"
        >
          {{ $t('menu.blog') }}
        </b-navbar-item>
        <b-navbar-dropdown
          :value="this.$i18n.locale"
          :label="$t('menu.language')"
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
