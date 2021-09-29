<template>
  <v-snackbar v-model="snackbar" :timeout="timeout">
    {{ text }}

    <template #action="{ attrs }">
      <v-btn color="blue" text v-bind="attrs" @click="snackbar = false">
        Close
      </v-btn>
    </template>
  </v-snackbar>
</template>

<script>
export default {
  data: () => ({
    snackbar: false,
    text: '',
    timeout: 5000,
  }),
  methods: {
    showAlert(text) {
      this.text = text
      this.snackbar = true
    },
  },
}
</script>
