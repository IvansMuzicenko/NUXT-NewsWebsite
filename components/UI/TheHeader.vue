<template>
  <div>
    <v-app-bar>
      <v-toolbar-title class="px-16"
        ><nuxt-link to="/">News</nuxt-link></v-toolbar-title
      >
      <v-btn class="mx-1"><nuxt-link to="/">Home</nuxt-link></v-btn>
      <v-btn class="mx-1"><nuxt-link to="/news">News</nuxt-link></v-btn>
      <v-btn class="mx-1"
        ><nuxt-link to="/contact-us">Contact us</nuxt-link></v-btn
      >
    </v-app-bar>
  </div>
</template>

<style lang="scss" scoped>
nuxt-link {
  text-decoration: none;
}
</style>
