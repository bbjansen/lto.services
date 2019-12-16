<template>
  <section class="section is-paddingless">
    <div class="tile is-ancestor" style="padding-top: 40px;">
      <div class="tile is-vertical is-8">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-danger is-radiusless">
              <p class="title">
                {{ $t('tile.consult.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('tile.consult.services')"
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
                {{ $t('tile.system.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('tile.system.services')"
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
                {{ $t('tile.software.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('tile.software.services')"
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
                {{ $t('tile.analysis.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('tile.analysis.services')"
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
                {{ $t('tile.saas.title') }}
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('tile.saas.services')"
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
                {{ $t('tile.about.title') }}
              </p>

              <p class="subtitle has-text-justified">
                {{ $t('tile.about.message') }}
              </p>

              <b-button
                tag="nuxt-link"
                to="/about"
                type="is-white"
                expanded
                outlined
              >
                {{ $t('tile.about.more') }}
              </b-button>
            </div>
          </article>
        </div>
        <div class="tile is-parent">
          <article class="tile is-child notification is-clean is-radiusless">
            <p class="title">
              {{ $t('tile.contact.title') }}
            </p>

            <p class="subtitle" style="white-space: pre-line">
              {{ $t('tile.contact.message') }}
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
                href="#"
                type="is-dark"
              >
                discord
              </b-button>
              <b-button
                tag="a"
                href="#"
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
