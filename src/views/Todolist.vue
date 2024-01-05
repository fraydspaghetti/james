<template>
  <div class="container">
    <div class="title">
      <h1>Todo App</h1>
    </div>
    <div class="actions">
      <form @submit.prevent="addTask">
        <button type="submit">Add</button>
        <input type="text" placeholder="Add Task" v-model="task" required>
        <input type="text" placeholder="Search Task" v-model="searchQuery">
      </form>
    </div>
    <div class="tasks">
      <div
        class="task-items"
        v-for="todo in filteredTask"
        :key="todo.id"
        @click="doneTask(todo.id)"
      >
        <p :class="{ done: todo.status }">{{ todo.details }}</p>
        <button class="done-btn">Done</button>
        <button class="remove-btn" @click="removeTask(todo.id)">Remove</button>
      </div>
      <div class="footerbut">
        <button class="clear-btn" @click="clearTask" style="display: inline;">Clear All Tasks</button>
        <router-link to="projects">
        <button class="back-btn" @click="backbutton" style="display: inline;">BACK TO PORTFOLIO</button>
      </router-link>
      </div>
      
    </div>
  </div>
</template>

<script>
import { v4 as uuidv4 } from 'uuid';

export default {
  data() {
    return {
      task: '',
      searchQuery: '',
      todos: [],
    };
  },
  methods: {
    addTask() {
      if (!this.task.trim()) {
        return;
      }

      const taskExists = this.todos.some((task) => task.details === this.task);

      if (taskExists) {
        alert('Task already exists');
      } else {
        const newTask = {
          id: uuidv4(),
          details: this.task,
          status: false,
        };
        this.todos.unshift(newTask);
        this.task = '';
      }
    },
    removeTask(id) {
      const index = this.todos.findIndex((todo) => todo.id === id);

      if (index !== -1) {
        const confirmed = window.confirm('Are you sure you want to remove this task?');

        if (confirmed) {
          this.todos.splice(index, 1);
        }
      }
    },
    doneTask(id) {
      const done = this.todos.find((todo) => todo.id === id);
      if (done) {
        done.status = !done.status;
      }
    },
    clearTask() {
      const confirmed = window.confirm('Are you sure you want to clear all tasks?');

      if (confirmed) {
        this.todos = [];
      }
    },
  },
  computed: {
    allTask() {
      return this.todos.length > 0;
    },
    filteredTask() {
      return this.todos.filter((todo) => {
        return todo.details.toLowerCase().includes(this.searchQuery.toLowerCase());
      });
    },
  },
};
</script>

<style scoped>
  .container {
    max-width: 558px;
    margin: 0 auto;
    padding: 20px;
  }

  .title {
    text-align: center;
    font-size: 28px;
    margin-bottom: 20px;
  }

  .actions form {
    display: flex;
    justify-content: space-between;
  }

  .actions input[type="text"] {
    flex: 1;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin-right: 10px;
  }

  .actions button[type="submit"] {
    background-color: #3498db;
    color: #fff;
    border: 0;
    border-radius: 5px;
    padding: 10px 20px;
    cursor: pointer;
  }

  .tasks .task-items {
    display: flex;
    align-items: center;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 10px 0;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  .tasks .task-items:hover {
    background-color: #f2f2f2;
  }

  .tasks p {
    flex: 1;
    margin: 0;
    padding: 10px;
    font-size: 18px;
  }

  .tasks .done-btn,
  .tasks .remove-btn {
    background-color: #e74c3c;
    color: #fff;
    border: 0;
    border-radius: 5px;
    padding: 10px 20px;
    cursor: pointer;
  }

  .tasks .done-btn {
    background-color: #3498db;
  }

  .clear-btn {
    background-color: #333;
    color: #fff;
    border: 0;
    border-radius: 5px;
    padding: 10px 20px;
    cursor: pointer;
    margin-left: auto;
    margin-top: 20px;
  }

  .done {
    text-decoration: line-through;
  }
  .footerbut{
    
  }
  .back-btn{
    background-color: #333;
    color: #fff;
    border: 0;
    border-radius: 5px;
    padding: 10px 20px;
    cursor: pointer;
    float: right;
    margin-top: 20px;
    margin-right: 10px;
  }
</style>
