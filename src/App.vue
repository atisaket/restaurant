<template>
  <div class="layout-transparent mdl-layout mdl-js-layout">
    <header class="mdl-layout__header mdl-layout__header--transparent">
      <div class="mdl-layout-icon"></div>
      <div class="mdl-layout__header-row">
        
        <!-- Title -->
        <span class="mdl-layout-title">Q's app</span>
        <!-- Add spacer, to align navigation to the right -->
        <div class="mdl-layout-spacer"></div>
        <!-- Navigation -->
        <nav class="mdl-navigation">
          <router-link class="mdl-navigation__link" to="/" @click.native="hideMenu">Home</router-link>
          <router-link class="mdl-navigation__link" to="/todo" @click.native="hideMenu">Todo</router-link>
          <router-link class="mdl-navigation__link" to="/todo" @click.native="hideMenu">Yelp</router-link>
        </nav>
      </div>
    </header>
    <div class="mdl-layout__drawer">
      <span class="mdl-layout-title">Q's app</span>
      <nav class="mdl-navigation">
        <router-link class="mdl-navigation__link" to="/" @click.native="hideMenu">Home</router-link>
        <router-link class="mdl-navigation__link" to="/todo" @click.native="hideMenu">Todo</router-link>
        <router-link class="mdl-navigation__link" to="/todo" @click.native="hideMenu">Yelp</router-link>
      </nav>
    </div>
    <!--<div aria-expanded="true" role="button" tabindex="0" class="mdl-layout__drawer-button">
      <i class="material-icons"></i> adding to see if git works
      </div>-->
    <main class="mdl-layout__content" style="background-color: transparent">
      <div class="page-content">
        <div class="app">
          <router-view></router-view>
        </div>
      </div>
      
    </main>
  </div>
</template>

<script>
  require('material-design-lite')
  import Todo from './components/Todo'
  import Home from './components/Home'
  
export default {
    name: 'app',
    methods: {
      hideMenu: function () {
        document.getElementsByClassName('mdl-layout__drawer')[0].classList.remove('is-visible')
        document.getElementsByClassName('mdl-layout__obfuscator')[0].classList.remove('is-visible')
      }
    },
    components: { Todo, Home }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/icon?family=Material+Icons');
  @import url('https://code.getmdl.io/1.3.0/material.blue-red.min.css');

  .layout-transparent {
  background: url('./assets/sunset.jpg') center / cover;
}
.layout-transparent .mdl-layout__header,
.layout-transparent .mdl-layout__drawer-button {
  /* This background is dark, so we set text to white. Use 87% black instead if
     your background is light. */
  color: white;
}
/*#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
</style>
