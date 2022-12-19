<template>
  <div>
    <app-input-todo></app-input-todo>
    <app-todo-list :todos="todos"></app-todo-list>
  </div>
</template>

<script>
import InputTodo from "./components/InputTodo.vue";
import TodoList from "./components/TodoList.vue";
export default {
  data: function () {
    return {
      newNoteData: "",
      todos: [
        {
          todo: "Go to Gym",
          description: "Go to celebrity gym",
          status: "todo",
        },
        {
          todo: "Make birthday Cake",
          description: "Make birthday cake for father's day",
          status: "ongoing",
        },
        {
          todo: "Final exam",
          description: "Prepare for school final exam next week",
          status: "completed",
        },
        {
          todo: "Graduation Day",
          description: "Prepare graduation day this week",
          status: "ongoing",
        },
      ],
    };
  },
  components: {
    "app-input-todo": InputTodo,
    "app-todo-list": TodoList,
  },
};
</script>

<style>
/** Body Style **/
body {
  font-family: "Open Sans", sans-serif;
}

/** Button Style **/
button:hover {
  cursor: pointer;
}
</style>