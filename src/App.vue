<script setup>
import Search from "./components/Search.vue";
import Todos from "./components/Todos.vue";
import TodoApp from "./components/TodoApp.vue";
</script>

<template>
  <div>
    <div id="header">
      <Search msg="Hello word" />
    </div>
    <div id="main-container"></div>
  </div>
</template>
<script>
export default {
  name: "App",
  components: {
    Search,
    Todos,
    TodoApp,
  },
  data() {
    return {
      todos: [
        {
          id: 0,
          title: "comprar la cena",
          completed: false,
        },
      ],
      copyTodos: [],
    };
  },
  created() {
    this.copyTodos = [...this.todos];
  },
};
</script>
<style scoped></style>
