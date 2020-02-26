<template>
  <div>
    <h2>My Todo List</h2>
    <ul>
      <li v-bind:key="todo.id" v-for="todo in todos">
        <Todo :todo="todo" />
      </li>
    </ul>
  </div>
</template>
<script>

import Todo from './Todo';
export default {
  name: 'Todolist',
  components: {
    Todo
  },
  props: [
    "todos"
  ]
}
</script>

<style scoped>
</style>