<template>
  <section class="section">
    <div class="notification is-dark">
      <p class="title">
        {{ $t('about.title') }}
      </p>

      <p class="subtitle has-text-justified">
        {{ $t('about.message') }}
      </p>
    </div>
  </section>
</template>

<script>

export default {
  name: 'About'
}
</script>
