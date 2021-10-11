<template>
  <li>
    <span v-bind:class="{ done: todo.completed }">
      <input type="checkbox" v-on:change="todo.completed = !todo.completed" />
      <strong>{{ index + 1 }}</strong>
      {{ upperCase(todo.title) }}
    </span>
    <button v-on:click="$emit('remove-todo', todo.id)">&times;</button>
  </li>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true,
    },
    index: Number
  },
  methods: {
    upperCase(value) {
      return value.toUpperCase()
    }
  }
};
</script>

<style scoped>
li {
  display: flex;
  justify-content: space-between;
  border: 1px solid black;
  margin-bottom: 5px;
  padding: 5px;
}
input {
  margin-right: 10px;
}
.done {
  text-decoration: line-through;
}
</style>