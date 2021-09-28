<template>
  <v-app>
    <ui-the-header />
    <ui-message-alert ref="snackbar" />
    <v-main>
      <v-container class="d-flex justify-center px-16">
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>
