<template>
  <div class="root-container">
    <form @submit="addTodo" class="form">
      <input placeholder="Enter new todo" type="text" v-model="typedTodo" />
      <button type="submit">Add todo</button>
    </form>
    <ul class="list" v-show="hasTodos">
      Remaining todos
      <li v-for="todo in todos" :key="todo.id" class="list-item">
        <div class="todo">
          <span>{{ todo.data }}</span>
          <button @click="completeThisTodo(todo)">Complete</button>
        </div>
      </li>
    </ul>
    <ul class="list" v-show="hasCompletedTodos">
      Completed todos
      <li v-for="todo in completedTodos" :key="todo.id" class="list-item">
        <div class="todo">
          <span>{{ todo.data }}</span>
          <button @click="uncompleteTodo(todo)">Un-complete</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
const createTodo = (todo, id) => ({ data: todo, id: id ?? Date.now() });

export default {
  name: 'HelloWorld',
  data() {
    return {
      todos: [{ data: 'hello world', id: Date.now() }],
      completedTodos: [],
      typedTodo: '',
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      if (this.typedTodo) {
        this.todos.unshift(createTodo(this.typedTodo));
        this.typedTodo = '';
      }
    },
    completeThisTodo(todoData) {
      this.todos = this.todos.filter(todo => todo.id !== todoData.id);
      this.completedTodos.unshift(createTodo(todoData.data, todoData.id));
    },
    uncompleteTodo(todoData) {
      this.completedTodos = this.completedTodos.filter(
        todo => todo.id !== todoData.id
      );
      this.todos.unshift(createTodo(todoData.data, todoData.id));
    },
  },
  computed: {
    hasTodos() {
      return this.todos.length > 0;
    },
    hasCompletedTodos() {
      return this.completedTodos.length > 0;
    },
  },
};
</script>

<style lang="scss" scoped>
.root-container {
  width: 100%;
  height: 100%;
  overflow-y: auto;
  padding: 40px;
}

.form {
  margin-bottom: 2rem;
}

.list {
  margin-bottom: 1rem;
}

.list-item {
  margin-bottom: 0.5rem;
  margin-left: 1rem;
}

.todo {
  display: flex;
  align-items: stretch;
  button {
    margin-left: 10px;
  }
}
</style>
