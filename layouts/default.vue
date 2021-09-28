<template>
  <v-app>
    <the-header></the-header>
    <v-main>
      <v-container class="d-flex justify-center px-16">
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Vue from 'vue'
// eslint-disable-next-line import/no-named-as-default
import VueSimpleAlert from 'vue-simple-alert'
import TheHeader from '../components/UI/TheHeader.vue'
Vue.use(VueSimpleAlert)
export default {
  components: { TheHeader },
}
</script>

<style lang="scss" scoped>
//
</style>
