/* eslint-disable */
<template>
  <div id="app">
     <!-- Render the components -->
    <!-- TodoList -->
    <h1 class="ui dividing centered header">Vue.js Todo App </h1>
    <div class="ui three column centered grid">
      <div class="column">
        <todo-list v-bind:todos="todos"></todo-list>
        <create-todo v-on:add-todo="addTodo"></create-todo>
      </div>
    </div>
  </div>
</template>

<script>
import TodoList from './components/TodoList';
import CreateTodo from './components/CreateTodo';

export default {
  name: 'App',
  components: {
    TodoList, CreateTodo
    // Add a reference to the the component here
  },

  // data function makes data available to the template
  data()  {
    return {
      todos: [{
        title: 'Todo A',
        project: 'Project A',
        done: false,
      }, {
        title: 'Todo B',
        project: 'Project B',
        done: true,
      }, {
        title: 'Todo C',
        project: 'Project C',
        done: false,
      }],
    };
  },

  methods: {
    addTodo(newTodo) {
      this.todos.push(newTodo);
    },
  }
};

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
