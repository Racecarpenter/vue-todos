<template>
  <div class="todo-input">
    <input type="text" v-model="newTodo">
    <button v-on:click="addTodo">Add</button>
  </div>
</template>

<script>
export default {
  name: 'todo-input',
  data () {
    return {
      newTodo: ''
    }
  },
  methods: {
    addTodo() {
      this.$emit('addTodo', this.newTodo)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
