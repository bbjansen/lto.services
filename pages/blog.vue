<template>
  <section class="section is-paddingless">
    <div class="tile is-ancestor" style="padding-top: 40px;">
      <div class="tile is-vertical">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification is-dark is-radiusless">
              <p class="title">
                Blog Post
              </p>
              <b-taglist>
                <b-tag
                  v-for="item in $t('tile.consult.services')"
                  v-bind:key="item"
                  size="is-medium"
                  type="is-white"
                >
                  {{ item }}
                </b-tag>
              </b-taglist>
            </article>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'Projects',

  components: {

  }
}
</script>
