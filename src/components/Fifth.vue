<script>
  let id = 0
  export default {
    data() {
      return {
        newTodo: '',
        hideCompleted: false,
        todos: [
          { id : 0, text : "something", done : false }
        ]
      }
    },
    computed: {
      filteredTodos: function() {
        return this.hideCompleted ? this.todos.filter((t) => !t.done) : this.todos
      }
    },
    methods: {
      addTodo() {
        if (this.newTodo != '') {
          this.todos.push({ id: id++, text: this.newTodo, done: false })
        }
        this.newTodo = ''
      },
      removeTodo(todo) {
        this.todos = this.todos.filter((t) => t !== todo)
      },
    }
  }
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Add new TODO</button>
  </form>
  <ul>
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done">
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <button @click="removeTodo(todo)" type="button" name="button">X</button>
    </li>
  </ul>
  <button @click="hideCompleted = !hideCompleted">{{ hideCompleted ? "Show all" : "Hide completed" }}</button>
</template>

<style media="screen">
.done {
  text-decoration: line-through;
}
</style>
