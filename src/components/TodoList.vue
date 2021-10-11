<template>
  <div>
    <ul>
      <TodoItem
        v-for="(todo, index) of todos"
        :key="todo.id"
        v-bind:todo="todo"
        v-bind:index="index"
        v-on:remove-todo="removeTodo"
      />
    </ul>
  </div>
</template>

<script>
import TodoItem from "@/components/TodoItem";
export default {
  components: {
    TodoItem,
  },
  props: ["todos"],
  methods: {
    removeTodo(id) {
      this.$emit("remove-todo", id);
    },
  },
};
</script>

<style scoped>
ul {
  text-decoration: none;
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>