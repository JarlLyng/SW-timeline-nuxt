<template>
<div>
  <Hero />
  <Timeline :posts="posts" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const posts = await $content('releases', params.slug)
    .sortBy('year', 'asc')
      .fetch()
    return {
      posts,
    }
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' },
      ],
    }
  },
}
</script>