<template>
  <section class="section">
    <div class="tile is-ancestor">
      <div class="tile is-vertical is-8">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-danger is-radiusless">
              <p class="title">
                {{ $t('tile.consult') }}
              </p>
              <p class="subtitle">
                {{ $t('tile.consult_text') }}
              </p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child notification is-info is-radiusless">
              <p class="title">
                {{ $t('tile.system') }}
              </p>
              <p class="subtitle">
                {{ $t('tile.system_text') }}
              </p>
            </article>
          </div>
        </div>
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-warning is-radiusless">
              <p class="title">
                {{ $t('tile.dev') }}
              </p>
              <p class="subtitle">
                {{ $t('tile.dev_text') }}
              </p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child notification is-success is-radiusless">
              <p class="title">
                {{ $t('tile.analysis') }}
              </p>
              <p class="subtitle">
                {{ $t('tile.analysis_text') }}
              </p>
            </article>
          </div>
        </div>
        <div class="tile is-parent">
          <article class="tile is-child notification is-clean is-radiusless">
            <p class="title">
              {{ $t('tile.contact') }}
            </p>
            <p class="subtitle">
              {{ $t('tile.contact_text') }}
            </p>
          </article>
        </div>
      </div>
      <div class="tile is-parent">
        <article class="tile is-child notification is-dark is-radiusless">
          <div class="content">
            <p class="title">
              {{ $t('tile.about') }}
            </p>
            <p class="subtitle">
              {{ $t('tile.about_text') }}
            </p>
            <div class="content">
              <!-- Content -->
            </div>
          </div>
        </article>
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
