<template>
  <div class="todos_container">
    <div class="todo_list">
        <app-todo-title :title="todoTitle[0]" :dataLength="todos.filter((data) => data.status === 'todo')"></app-todo-title>
      <div class="todos" v-for="todo in todos" :key="todo.id">
        <app-todo-item v-if="todo.status === 'todo'" :data="todo"></app-todo-item>
      </div>
    </div>

    <div class="todo_list todo_center">
      <app-todo-title :title="todoTitle[1]" :dataLength="todos.filter((data) => data.status === 'ongoing')"></app-todo-title>
      <div class="todos" v-for="todo in todos" :key="todo.id">
        <app-todo-item v-if="todo.status === 'ongoing'" :data="todo"></app-todo-item>
      </div>
    </div>

    <div class="todo_list">
      <app-todo-title :title="todoTitle[2]" :dataLength="todos.filter((data) => data.status === 'completed')"></app-todo-title>
      <div class="todos" v-for="todo in todos" :key="todo.id">
        <app-todo-item v-if="todo.status === 'completed'" :data="todo"></app-todo-item>
      </div>
    </div>
  </div>
  <!-- End List Todo -->
</template>

<script>
import TodoItem from "./TodoItem.vue"
import TodoTitle from "./TodoTitle.vue"

export default {
    props: ["todos"],
    data: function() {
        return {
            todoTitle: ["Todo", "In Progress", "Completed"],
        }
    },
    components: {
        "app-todo-item": TodoItem,
        "app-todo-title": TodoTitle
    }
}
</script>

<style>
/** Start Todo List Style **/
    .todos {
        display: flex;
        flex-direction: column;
    }
 
    .todos_container {
        display: flex;
        justify-content: center;
        margin-top: 35px;
        margin-bottom: 35px;
    }

    .todo_list {
        border:0;
        box-shadow:0 0 15px 4px rgba(0,0,0,0.06);
        padding-left: 10px;
        padding-right: 10px;
        border-radius: 15px;
    }

    .todo_center {
        margin-right: 40px;
        margin-left: 40px;
    }
    /** End Todo List Style **/
</style>