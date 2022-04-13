<template>
  <div id="app">
    <div class="container">
      <div class="block">
        <input v-model="form.text" type="text">
        {{form.text}}
        <button @click="getLowerText">Call method</button>
        {{textLower}}
        {{toLower}}
      </div>

      <div class="block">
        <button @click="show =! show">Show content</button>
        <p v-if="show">Some content</p>
      </div>
    </div>
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
      textLower: '',

      show: false
    }
  },
  computed: {
    toLower () {
      return this.form.text.toLowerCase()
    }
  },
  methods: {
    getText () {
      alert(`Hello ${this.text}`)
    },
    getLowerText () {
      this.textLower = this.form.text.toLowerCase()
    }
  },
}
</script>

<style lang="sass">
.container
  max-width: 1200px
  margin: 0 auto
  display: flex
  flex-direction: column
  .block
    border:  1px solid #cecece
    border-radius: 10px
    padding: 10px
    &:not(:first-child)
      margin-top: 10px
</style>
