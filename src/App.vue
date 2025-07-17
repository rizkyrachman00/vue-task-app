<script lang="ts" setup>
import { ref } from 'vue'
import TaskForm from './components/TaskForm.vue'
import type { Task } from './types';
import TaskList from './components/TaskList.vue';

const message = ref('Task App')
const tasks = ref<Task[]>([])

function addTask(newTask: string) {
  tasks.value.push({
    id: crypto.randomUUID(),
    title: newTask,
    done: false
  })
}

</script>

<template>
  <main>
    <h1>{{ message }}</h1>
    <TaskForm @add-task="addTask" />
    <h3>There are {{ tasks.length }} task.</h3>
    <TaskList :tasks />
  </main>
</template>

<style>
main {
  max-width: 800px;
  margin: 1rem auto;
}

.button-container {
  display: flex;
  justify-content: end;
}
</style>
