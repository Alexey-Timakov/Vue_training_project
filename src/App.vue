<template>
  <div id="app">
    <h1>Todo application</h1>
    <hr>
    <!-- <AddTodo
        @add-todo="addTodo"
    />
    <hr />
    <TodoList
      v-bind:todos="todos"
      @remove-todo="removeTodo"
    /> -->
    <router-view />
  </div>
</template>

<script>
// import TodoList from "@/components/TodoList";
// import AddTodo from "@/components/AddTodo";

export default {
  name: "App",
  components: {
    // TodoList,
    // AddTodo
  },
  // data() {
  //   return {
  //     todos: [],
  //   };
  // },
  // methods: {
  //   removeTodo(id) {
  //     this.todos = this.todos.filter(todo => todo.id != id)
  //   },
  //   addTodo(newTodo) {
  //     this.todos.push(newTodo);
  //   }
  // },
  // mounted() {
  //   fetch('https://jsonplaceholder.typicode.com/posts?_limit=5')
  //   // fetch('https://jsonplaceholder.typicode.com/posts')
  //   .then((response) => response.json())
  //   // .then((json) => this.todos = json.slice(0, 5));
  //   .then((json) => this.todos = json);
  // }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>