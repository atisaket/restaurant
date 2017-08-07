<template>
  <div class="home mdl-grid">
    <div class="mdl-cell mdl-cell--1-col">
      
    </div>
    <div class="mdl-cell mdl-cell--10-col mdl-color--white mdl-shadow--2dp">
      <img src="../assets/logo.png">
    <h1>{{ msg }}</h1>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
.home {
  color: black;
}
ul {
  list-style-position: inside;
}


a {
  color: #42b983;
}
</style>
