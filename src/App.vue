<template>
  <div id="app">
    <button @click="getText">Call method</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  methods: {
    getText () {
      alert('Hello')
    }
  }
}
</script>
