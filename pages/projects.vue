<template>
  <section class="section is-paddingless">
    <div class="tile is-ancestor" style="padding-top: 40px;">
      <div class="tile">
        <div
          class="tile"
          v-for="post in posts"
          v-bind:key="post"
        >
          <div class="tile is-parent">
            <article
              class="tile is-child notification is-dark is-radiusless"
            >
              <p class="title">
                {{ post.title }}
              </p>

              <p class="subtitle">
                {{ post.excerpt }}
              </p>
              <b-button
                :href="post.url"
                tag="a"
                type="is-white"
                expanded
                outlined
              >
                Read More
              </b-button>
            </article>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import GhostContentAPI from '@tryghost/content-api'

const api = new GhostContentAPI({
  url: 'https://cms.lto.services',
  key: 'ce375a1758e6ca83e6a7889c16',
  version: 'v3'
})

export default {
  name: 'Projects',
  components: {
  },
  async asyncData () {
    const posts = await api.posts.browse({ slug: 'projects' })
    return { posts }
  }
}
</script>
