<script lang="ts" setup>
import { ref } from 'vue'

const emit = defineEmits<{
  addTask: [newTask: string]
}>()

const newTask = ref('')
const error = ref('')

function formSubmitted() {
  if (newTask.value.trim()) {
    emit('addTask', newTask.value)
    newTask.value = ''
  }
  else {
    error.value = 'Task cannot be empty'
  }
}

</script>

<template>
  <form @submit.prevent="formSubmitted">
    <label>
      New Task
      <input 
      v-model="newTask" 
      type="text" 
      name="newTask" 
      :aria-invalid="!!error || undefined"
      @input="error = ''"
      >
      <small v-if="error" id="invalid-helper">
        {{ error }}
      </small>
    </label>
    <div class="button-container">
      <button>Add</button>
    </div>
  </form>
</template>

<style scoped></style>