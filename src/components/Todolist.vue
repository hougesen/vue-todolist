<template>
  <div class="todoContainer">
    <h1>Todolist</h1>
    <input type="text" placeholder="Enter a thing to do..." v-model="todo" @keyup.enter="addTodo" required />
    <ul>
      <li v-for="(element, index) in todos" :key="element" class="listElement">
        {{ element }}
        <i class="fa fa-minus-circle" @click="removeTodo(index)"></i>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'Todolist',
    data() {
      return {
        todo: '',
        todos: [],
      };
    },

    beforeMount() {
      localStorage.getItem('todos') != null
        ? (this.todos = JSON.parse(localStorage.getItem('todos')))
        : (this.todos = []);
    },

    methods: {
      addTodo() {
        this.todos.push(this.todo);
        this.todo = '';
        this.saveLocalStorage();
      },

      removeTodo(id) {
        this.todos.splice(id, 1);
        this.saveLocalStorage();
      },

      saveLocalStorage() {
        let jsonTodos = JSON.stringify(this.todos);
        localStorage.setItem('todos', jsonTodos);
      },
    },
  };
</script>

<style scoped la>
  @import 'https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css';
  .todoContainer {
    width: 50%;
    margin: auto;
  }

  h1 {
    text-align: center;
    margin: 20px 0 20px 0;
  }

  input {
    width: 100%;
    font-size: 1.4em;
    border: none;
    padding: 10px;
    background-color: #252626;
    color: white;
  }

  .listElement {
    background-color: #e0edf4;
    font-size: 1.4em;
    border-left: 10px solid #3eb3f6;
    padding: 10px;
    margin-top: 5px;
    color: grey;
    list-style-type: none;
  }

  .fa-minus-circle {
    cursor: pointer;
    float: right;
  }
</style>
