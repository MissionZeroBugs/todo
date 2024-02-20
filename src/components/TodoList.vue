<script setup lang="ts">
import PrimeCheckbox from "primevue/checkbox";
import { ref } from "vue";
const props = defineProps<{ tasks: string[]; todoListTitle: string }>();
const selectedTasks = ref([]);
</script>

<template>
  <div class="todo-list-title">
    {{ todoListTitle }}
  </div>
  <div v-for="task of tasks" :key="task" class="flex align-items-center py-2">
    <PrimeCheckbox
      v-model="selectedTasks"
      :inputId="task"
      name="task"
      :value="task"
      class="mr-2"
    />
    <label :for="task">{{ task }}</label>
  </div>
</template>

<style>
.todo-list-title {
  font-size: 30px;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
