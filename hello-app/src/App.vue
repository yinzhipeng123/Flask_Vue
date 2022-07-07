<template>
  <div id="app">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
var axios = require('axios');

export default {
  name: 'app',
  data () {
    return {
      msg: ''
    }
  },
  mounted() {
    axios.get('/api/hello')
      .then(response => this.msg = response.data.data)
  }
}
</script>

<style>

</style>
