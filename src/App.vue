<template>
  <div id="app">
    <h1>{{title}}</h1>
    <div v-for="(note, index) in notes" :key="index">
      {{note}}
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {},
  data () {
    return {
      title: 'Notes App',
      notes: [
        {
          title: 'First',
          description: 'some text',
          date: new Date(Date.now()).toLocaleString()
        },
        {
          title: 'Second',
          description: 'some text',
          date: new Date(Date.now()).toLocaleString()
        },
        {
          title: 'Third',
          description: 'some text',
          date: new Date(Date.now()).toLocaleString()
        },
      ]
    }
  }
}
</script>
