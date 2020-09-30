<template>
  <form @submit="addNewTodo">
    <label name="newTodo">New Todo</label>
    <input
      type="text"
      v-model="newTodo"
      id="newTodo"
      placeholder="add new todo"
    />
    <button type="submit">Submit</button>
  </form>
</template>

<script>
import { ref } from 'vue';
// eslint-disable-next-line
const newTodo = ref('');
console.log(newTodo.value);
export default {
  setup() {
    function addNewTodo(e) {
      e.preventDefault();
      console.log('adding a new todo ');
    }
    return { newTodo, addNewTodo };
  },
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
