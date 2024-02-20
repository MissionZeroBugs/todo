<script setup lang="ts">
import HomeNavbar from "./components/HomeNavbar.vue";
import TodoList from "./components/TodoList.vue";
</script>

<template>
  <HomeNavbar :items="['Home', 'Tasks', 'Reminders', 'Calendar', 'About']" />
  <TodoList
    :tasks="['Center the div!!!', 'Clean the room', 'Cook dinner', 'Watch JJK']"
    todo-list-title="My Todo List"
  />
</template>
