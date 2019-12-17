<template>
  <section class="section">
    <div v-if="posts.length === 0">
      <div class="columns is-mobile is-centered">
        <div class="column is-half has-text-centered">
          <p class="subtitle">
            {{ $t('blog.empty') }}
          </p>
        </div>
      </div>
    </div>
    <div v-else>
      <div class="tile is-ancestor" style="padding-top: 40px;">
        <div class="tile">
          <div
            v-for="post in posts"
            v-bind:key="post.id"
            class="tile"
          >
            <div class="tile is-parent">
              <article
                :class="randomColor()"
                class="tile is-child notification is-radiusless"
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
                  {{ $t('blog.more') }}
                </b-button>
              </article>
            </div>
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
  name: 'Blogs',
  async asyncData () {
    const posts = await api.posts.browse({ filter: 'tag:blog' })
    return { posts }
  },
  methods: {
    randomColor () {
      const colors = ['dark', 'info', 'success', 'warning', 'danger', 'clean', 'fresh']
      return 'is-' + colors[Math.floor(Math.random() * colors.length)]
    }
  }
}
</script>
