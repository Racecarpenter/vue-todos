<template>
  <div class="todo-list">
    <ul>
      <li v-for="todo in todos">{{todo.title}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'todo-list',
  props: ['todos'],
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
