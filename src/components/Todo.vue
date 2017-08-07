<template>
  <div class="todo">
    <div class="mdl-grid">
      <div class="mdl-cell mdl-cell--11-col">
        <h1>{{msg}}</h1>
      </div>
    </div>
    
    <hr />
    <div class="mdl-grid">
      <div class="mdl-cell mdl-cell--1-col">
        
      </div>
      <div class="mdl-cell mdl-cell--10-col">
        <ul class="list-item mdl-list" v-for="item in todoList">
        <li class="mdl-list__item">
          <span class="mdl-list__item-primary-content">
            {{item.item}}
          </span>
        </li>
      </ul>
      </div>
      
    </div>
    <hr />
    <form action="#" class="mdl-grid">
      <div class="mdl-cell mdl-cell--1-col">
        
      </div>
      <div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label mdl-cell mdl-cell--1-col">
        <input class="mdl-textfield__input" type="text" id="input" v-model="inputVal">
        <label class="mdl-textfield__label" for="input">Todo</label>
      </div>
    </form>
    <div class="mdl-grid">
      <div class="mdl-cell mdl-cell--1-col">
        
      </div>
      <div class="mdl-cell mdl-cell--1-col">
        <button v-on:click="addItem" class="mdl-button mdl-js-button mdl-button--raised mdl-button--colored">
          Add user
        </button>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'todo',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      todoList: [
        {item: 'Buy groceries'}
      ],
      inputVal: ''
    }
  },
  methods: {
    addItem: function () {
      this.todoList.push({item: this.inputVal})
      // alert('Add user called')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import url('https://fonts.googleapis.com/icon?family=Material+Icons');
  @import url('https://code.getmdl.io/1.3.0/material.blue-red.min.css');
h1, h2 {
  font-weight: normal;
}
.list-item {
  width: 300px;
}
ul {
  list-style-position: inside;
  align-items: left;
}


a {
  color: #42b983;
}
</style>
