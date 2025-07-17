<script lang="ts" setup>
  import { ref } from 'vue'

  // define reaktif value pada vue
  // seperti konsep state pada react
  // nilai bisa di update
  const message = ref('Hello World')

</script>

<template>
  <main>
    <h1>{{ message }}</h1>
  </main>
</template>

<style scoped>
  main {
    max-width: 800px;
    margin: 1rem auto;
  }
</style>
