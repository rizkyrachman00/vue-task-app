<script lang="ts" setup>
import { ref } from 'vue'

const message = ref('Task App')
const newTask = ref('')

</script>

<template>
  <main>
    <h1>{{ message }}</h1>
    <form>
      <label>
        New Task
        <input v-model="newTask" type="text" name="newTask">
      </label>
      <h3>{{ newTask }}</h3>
    </form>
  </main>
</template>

<style scoped>
main {
  max-width: 800px;
  margin: 1rem auto;
}
</style>
