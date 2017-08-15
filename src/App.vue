<template>
  <div id="app">
    <todo-input @addTodo="addTodo"></todo-input>
    <todo-list :todos="todos"></todo-list>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
import TodoInput from './components/TodoInput.vue'
let counter = 6;
export default {
  name: 'app',
  components: {
    TodoInput,
    TodoList
  },
  data () {
    return {
      todos: [
        {id: 1, title: 'do some things'},
        {id: 2, title: 'do the laundry'},
        {id: 3, title: 'play some horizon'},
        {id: 4, title: 'work the funk out'},
        {id: 5, title: 'sleeeeeeeeep'}
      ]
    }
  },
  methods: {
    addTodo: function(todo) {
      this.todos.push({id: counter, title: todo})
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
