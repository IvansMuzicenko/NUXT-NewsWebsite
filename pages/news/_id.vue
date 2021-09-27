<template>
  <div>
    <h1>{{ article.title }}</h1>
    <p>{{ article.description }}</p>
    <nuxt-content :document="article" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const id = params.id
    const article = await $content('news', id).fetch()
    return { article }
  },
}
</script>

<style lang="scss" scoped>
div {
  width: 60%;
}
</style>
