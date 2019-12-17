<template>
  <section class="section is-paddingless">
    <div v-if="posts.length === 0">
      <div class="columns is-mobile is-centered">
        <div class="column is-half has-text-centered">
          <p class="subtitle">
            {{ $t('projects.empty') }}
          </p>
        </div>
      </div>
    </div>
    <div v-else>
      <div
        v-for="(group, i) in groupPosts"
        v-bind:key="i"
        class="tile is-ancestor"
        style="padding-top: 40px;"
      >
        <div
          v-for="post in posts.slice(i * 3, (i + 1) * 3)"
          v-bind:key="post.id"
          class="tile"
        >
          <div class="tile">
            <div class="tile is-parent">
              <article
                :class="randomColor()"
                class="tile is-child notification is-radiusless"
              >
                <p class="title">
                  {{ post.title }}
                </p>

                <p class="subtitle has-text-justified" style="white-space: pre-line">
                  {{ post.excerpt }}
                </p>
                <b-button
                  :href="post.url"
                  tag="a"
                  type="is-black"
                  expanded
                  outlined
                >
                  {{ $t('projects.more') }}
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
  key: process.env.GHOST_API,
  version: 'v3'
})

export default {
  name: 'Projects',
  computed: {
    groupPosts () {
      return Array.from(Array(Math.ceil(this.posts.length / 3)).keys())
    }
  },
  async asyncData () {
    const posts = await api.posts.browse({ filter: 'tag:projects' })
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
