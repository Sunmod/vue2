<template>
  <div id="app">
    <input v-model="form.text" type="text">
    {{form.text}}
    <button @click="getLowerText">Call method</button>
    {{textLower}}
    <br>
    <hr>
    {{toLower}}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      text: ' some text',
      form: {
        text: ''
      },
      textLower: ''
    }
  },
  computed: {
    toLower () {
      return this.form.text.toLowerCase()
    }
  },
  methods: {
    getText () {
      // alert('Hello' + this.text)
      alert(`Hello ${this.text}`)
    },
    getLowerText () {
      this.textLower = this.form.text.toLowerCase()
    }
  },
}
</script>
