<template>
  <div id="app">
    <button @click="getText">Call method</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      text: ' some text'
    }
  },
  methods: {
    getText () {
      alert('Hello' + this.text)
    }
  }
}
</script>
