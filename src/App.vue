<template>
  <div id="app">
    <Todolist :todos="todos" />
    <AddTodo v-on:add-todo="addTodo"/>
  </div>
</template>

<script>
import Todolist from './components/Todolist';
import AddTodo from './components/AddTodo';

export default {
  name: 'app',
  components: {
    Todolist,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Daily Lift',
          completed: false
        },
        {
          id: 2,
          title: 'Programming Exercises',
          completed: false
        },
        {
          id: 3,
          title: 'Prep meals',
          completed: false
        },
        {
          id: 4,
          title: 'Design WolfWilderness',
          completed: false
        },
        {
          id: 5,
          title: 'Finish work',
          completed: false
        }
      ],
    }
  },
  methods: {
    addTodo(newTodoObj) {
      this.todos = [...this.todos, newTodoObj];
    }
  }
}
</script>

<style>

</style>
