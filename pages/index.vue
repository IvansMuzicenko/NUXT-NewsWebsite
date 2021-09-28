<template>
  <div>
    <h1>Welcome to News</h1>
    <p>
      All news will be published <nuxt-link to="/news">here</nuxt-link> as soon
      as posible for humans!
    </p>
    <p>
      Thanks for chosing our news portal! We are very apreciated to see you here
      :-)
    </p>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Home',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'The best News website, with highest ratings in the world',
      },
    ],
  },
}
</script>
