<template>
  <div>
    <section>
      <h1>Contact us</h1>
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
    </section>

    <section>
      <form @submit.prevent="submitForm()">
        <label for="email">E-mail:</label>
        <input id="email" v-model="email" type="email" />
        <br />
        <label for="tel">Tel. number:</label>
        <input id="tel" v-model="tel" type="tel" />
        <br />
        <label for="message"> Your message:</label>
        <br />
        <textarea id="message" v-model="message" rows="10"></textarea>
        <button type="submit">Send</button>
      </form>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return { email: '', tel: '', message: '' }
  },
  methods: {
    submitForm() {
      console.log('Submitted')
      this.email = this.tel = this.message = ''
    },
  },
}
</script>

<style scoped lang="scss">
input {
  border-block-color: black;
}
</style>
