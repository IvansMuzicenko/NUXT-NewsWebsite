<template>
  <v-app>
    <the-header></the-header>
    <v-main>
      <v-container class="d-flex justify-center">
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import TheHeader from '../components/UI/TheHeader.vue'
export default {
  components: { TheHeader },
}
</script>

<style lang="scss" scoped>
//
</style>
