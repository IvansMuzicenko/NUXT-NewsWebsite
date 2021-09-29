<template>
  <div>
    <h1 class="d-flex justify-center">All News</h1>
    <v-row>
      <v-card
        v-for="article in articles"
        :key="article.slug"
        class="col-12 my-3"
      >
        <v-row>
          <v-col lg="5">
            <v-img height="300" width="300" :src="article.image"></v-img>
          </v-col>
          <v-col lg="7">
            <v-card-title>
              {{ article.title }}
            </v-card-title>
            <v-card-subtitle>{{ article.description }}</v-card-subtitle>
            <v-card-actions>
              <v-btn :to="`/news/${article.slug}`" outlined rounded text>
                Read more
              </v-btn>
            </v-card-actions>
          </v-col>
        </v-row>
      </v-card>
    </v-row>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articles = await $content('news').sortBy('slug', 'desc').fetch()
    return { articles }
  },
  head: {
    title: 'All News',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'All news to the moment are available only on this page',
      },
    ],
  },
}
</script>

<style scoped>
ul {
  list-style: none;
}
</style>
