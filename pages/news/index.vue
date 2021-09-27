<template>
  <div id="news">
    All news
    <ul>
      <li v-for="article in articles" :key="article.slug">
        <nuxt-link :to="`news/${article.slug}`">
          {{ article.title }}
        </nuxt-link>
        <br />
        {{ article.description }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articles = await $content('news').sortBy('slug', 'desc').fetch()
    console.log(articles)

    return { articles }
  },
}
</script>

<style scoped>
ul {
  list-style: none;
}
</style>
