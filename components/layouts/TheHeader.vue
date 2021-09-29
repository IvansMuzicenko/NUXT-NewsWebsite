<template>
  <div>
    <v-app-bar>
      <v-toolbar-title class="mx-md-16" to="/"
        ><nuxt-link to="/">News</nuxt-link></v-toolbar-title
      >
      <v-spacer></v-spacer>
      <nav class="mr-md-10">
        <v-btn class="mx-1" to="/">Home</v-btn>
        <v-btn class="mx-1" to="/news">News</v-btn>
        <v-btn class="mx-1" to="/contact-us">Contact us</v-btn>
      </nav>
    </v-app-bar>
  </div>
</template>

<style lang="scss" scoped>
nuxt-link {
  text-decoration: none;
}
</style>
