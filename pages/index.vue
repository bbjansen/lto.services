<template>
  <section class="section is-paddingless">
    <div class="tile is-ancestor" style="padding-top: 40px;">
      <div class="tile is-vertical is-8">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-danger is-radiusless">
              <p class="title">
                {{ $t('services.consult.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('services.consult.services')"
                  v-bind:key="item"
                  size="is-medium"
                  type="is-dark"
                >
                  {{ item }}
                </b-tag>
              </b-taglist>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child notification is-info is-radiusless">
              <p class="title">
                {{ $t('services.system.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('services.system.services')"
                  v-bind:key="item"
                  size="is-medium"
                  type="is-dark"
                >
                  {{ item }}
                </b-tag>
              </b-taglist>
            </article>
          </div>
        </div>
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-warning is-radiusless">
              <p class="title">
                {{ $t('services.software.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('services.software.services')"
                  v-bind:key="item"
                  size="is-medium"
                  type="is-dark"
                >
                  {{ item }}
                </b-tag>
              </b-taglist>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child notification is-success is-radiusless">
              <p class="title">
                {{ $t('services.analysis.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('services.analysis.services')"
                  v-bind:key="item"
                  size="is-medium"
                  type="is-dark"
                >
                  {{ item }}
                </b-tag>
              </b-taglist>
            </article>
          </div>
        </div>
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-fresh is-radiusless">
              <p class="title">
                {{ $t('services.saas.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('services.saas.services')"
                  v-bind:key="item"
                  size="is-medium"
                  type="is-dark"
                >
                  {{ item }}
                </b-tag>
              </b-taglist>
            </article>
          </div>
        </div>
      </div>
      <div class="tile is-vertical">
        <div class="tile is-parent">
          <article class="tile is-child notification is-dark is-radiusless">
            <div class="content">
              <p class="title">
                {{ $t('about.title') }}
              </p>

              <p class="subtitle has-text-justified">
                {{ $t('about.message') }}
              </p>

              <b-button
                tag="nuxt-link"
                to="/about"
                type="is-white"
                expanded
                outlined
              >
                {{ $t('about.more') }}
              </b-button>
            </div>
          </article>
        </div>
        <div class="tile is-parent">
          <article class="tile is-child notification is-clean is-radiusless">
            <p class="title">
              {{ $t('contact.title') }}
            </p>

            <p class="subtitle" style="white-space: pre-line">
              {{ $t('contact.message') }}
            </p>
            <div class="buttons">
              <b-button
                tag="a"
                href="mailto:bobjansen@pm.me"
                type="is-dark"
              >
                e-mail
              </b-button>
              <b-button
                tag="a"
                href="https://t.me/ltoservices"
                type="is-dark"
              >
                telegram
              </b-button>
            </div>
          </article>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'HomePage',

  components: {

  }
}
</script>
