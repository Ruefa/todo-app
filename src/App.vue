<template>
  <div id="app">
    <button v-on:click="clicked">click mne </button>
    <ToDoList v-bind:items="todos" id="list"/>
    <ToDoList v-bind:items="todos" id="days"/>
  </div>
</template>

<script>
  import ToDoList from './components/to-do-list';

  export default {
    name: 'App',
    components: {
      ToDoList,
    },
    data () {
      return {
        todos: [
          {
            id: 1,
            msg: 'hello there again'
          },
          {
            id: 2,
            msg: 'hello there again... again'
          }
        ]
      }
    },
    methods: {
      clicked: function () {
        console.log(this.todos);
      }
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
#list {
  width: 45%;
  float:right;
}
#days {
  width: 45%;
  float:left;
}
</style>
