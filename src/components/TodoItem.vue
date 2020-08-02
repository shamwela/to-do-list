<template>
  <!-- If it is completed, the class 'is-completed' will be added -->
  <div class="todo-item" v-bind:class="{'is-completed': todo.completed}">
    <p>
      <!-- Add Event Listener -->
      <input type="checkbox" v-on:change="markComplete" />
      {{todo.title}}
      <!-- Add Click Listener and Send data to Todos -->
      <button @click="$emit('del-todo', todo.id)" class="del">x</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      // Toggle true & false
      this.todo.completed = !this.todo.completed;
    },
  },
};
</script>

<style scoped>
.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px dotted #ccc;
}

.is-completed {
  text-decoration: line-through;
}

.del {
  background: #ff0000;
  color: #fff;
  border: none;
  padding: 5px 9px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}
</style>