<script>
  let id = 0
  export default {
    data() {
      return {
        newTodo: '',
        todos: []
      }
    },
    methods: {
      addTodo() {
        if (this.newTodo != '') {
          this.todos.push({ id: id++, text: this.newTodo })
        }
        this.newTodo = ''
      },
      removeTodo(todo) {
        delete this.todos[todo.id]
      }
    }
  }
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Add new TODO</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
      <button @click="removeTodo(todo)" type="button" name="button">X</button>
    </li>
  </ul>
</template>
