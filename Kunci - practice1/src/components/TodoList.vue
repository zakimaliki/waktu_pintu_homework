<template>
  <div class="todos_container">
    <div class="todo_list">
      <div class="todo-title">
        <h1>Todo</h1>
        <h1>5</h1>
      </div>
      <div class="todos">
        <app-todo-item></app-todo-item>
      </div>
    </div>

    <div class="todo_list todo_center">
      <div class="todo-title">
        <h1>In Progress</h1>
        <h1>5</h1>
      </div>
      <div class="todos">
        <app-todo-item></app-todo-item>
      </div>
    </div>

    <div class="todo_list">
      <div class="todo-title">
        <h1>Completed</h1>
        <h1>5</h1>
      </div>
      <div class="todos">
        <app-todo-item></app-todo-item>
      </div>
    </div>
  </div>
  <!-- End List Todo -->
</template>

<script>
import TodoItem from "./TodoItem.vue"

export default {
    components: {
        "app-todo-item": TodoItem
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

    .todo-title {
        display: flex;
        justify-content: space-between;
        margin: 15px 20px 0px 20px;
        color: #3F51B5
    }

    .todo-title h1 {
        font-size: 20px;
        margin: 0px;
    }

    .todo-title h1:last-child {
        color: white;
        background-color: #3F51B5;
        padding-left: 9px;
        padding-right: 9px;
        padding-top: 4px;
        border-radius: 50px;
        font-size: 13px;
    }

    /** End Todo List Style **/
</style>