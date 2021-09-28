<template>
  <div>
    <h1 class="d-flex justify-center">Contact us</h1>
    <v-row class="mt-3">
      <v-card class="px-3 col-12">
        <v-card-title class="d-flex justify-center my-5"
          >Our info:</v-card-title
        >
        <p>
          Address:
          <a
            target="_blank"
            href="http://maps.google.com/maps?q=Russia,+Moscow,+Pushkina+street+228"
          >
            Russia, Moscow, Pushkina street 228</a
          >
        </p>
        <p>
          E-mail:
          <a target="_blank" href="mailto:ouremail@email.com"
            >ouremail@email.com</a
          >
        </p>
        <p>
          Phone: <a href="tel:+1337-228-335-709-705">+1337-228-335-709-705</a>
        </p>
      </v-card>

      <v-card class="px-3 col-12">
        <v-card-title class="d-flex justify-center my-5"
          >Send a message to our team:</v-card-title
        >
        <v-form v-model="valid" @submit.prevent="submitForm()">
          <v-container>
            <v-row>
              <v-col cols="12" md="6">
                <v-text-field
                  v-model="firstname"
                  :rules="nameRules"
                  :counter="10"
                  label="First name*"
                  required
                ></v-text-field>
              </v-col>

              <v-col cols="12" md="6">
                <v-text-field
                  v-model="lastname"
                  :rules="nameRules"
                  :counter="10"
                  label="Last name*"
                  required
                ></v-text-field>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12" md="6">
                <v-text-field
                  v-model="email"
                  :rules="emailRules"
                  label="E-mail*"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <v-text-field v-model="tel" label="Tel. number"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea v-model="message" :rules="messageRules" label="Message">
            </v-textarea>
          </v-container>
          <v-btn v-if="valid" type="submit">Send</v-btn>
        </v-form>
      </v-card>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    firstname: '',
    lastname: '',
    nameRules: [
      (v) => !!v || 'Name is required',
      (v) => v.length <= 10 || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      (v) => !!v || 'E-mail is required',
      (v) => /.+@.+/.test(v) || 'E-mail must be valid',
    ],
    tel: '',
    message: '',
    messageRules: [
      (v) => !!v || 'Message is required',
      (v) => v.length >= 20 || 'Message must be more than 20 characters',
    ],
  }),
  methods: {
    submitForm() {
      console.log('Submitted')
      this.firstname = this.lastname = this.email = this.tel = this.message = ''
      this.valid = true
      this.$alert(
        'Thanks for your feedback! We will answer you in nearest possible time!'
      )
      this.$router.push('/')
    },
  },
}
</script>
