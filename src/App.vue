<template>
  <div id="app">
    <Postslist v-bind:source="source"></Postslist>
  </div>
</template>

<script>

import Postslist from './components/Postslist'

export default {
  name: 'app',
  components: {
    Postslist
  },
  data () {
    return {
      source: ''
    }
  }
}
</script>

<style>
#app {
  padding-top: 20px
}
</style>
