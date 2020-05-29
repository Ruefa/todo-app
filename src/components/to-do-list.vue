<template>
  <div class="todo-container">
    <button v-on:click="addTodo" id="button-new-todo">press</button>
    <ToDoItem v-for="item in items" :key="item.id" :msg="item.msg"/>
  </div>
</template>

<script>
  import ToDoItem from './to-do-item';


  export default {
    name: 'to-do-list',
    props: {
      items: Array
    },
    components: {
      ToDoItem,
    },
    methods: {
      addTodo: function () {
        this.items.push({
          id: this.items.length + 1,
          msg: 'clicked button'
        })
      }
    }
  }
</script>

<style scoped>
  .todo-container {
    text-align: right;
    border: 2px solid black;
  }
  #button-new-todo {
    width: fill-available;
  }
</style>
