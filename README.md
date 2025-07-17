# Vue 3 + TypeScript + Vite

This template should help get you started developing with Vue 3 and TypeScript in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

Learn more about the recommended Project Setup and IDE Support in the [Vue Docs TypeScript Guide](https://vuejs.org/guide/typescript/overview.html#project-setup).

+++ setup project +++

- install pico css -> https://picocss.com/

<script setup lang="ts">

</script>

lang="ts" --> digunakan ketika menggunakan bahasa typescript
setup --> composition API VUE 3 (cara baru)

options API (cara lama)


run project dev phase --> `pnpm run dev`


<style scoped>
  main{
    
  }

</style>

scoped --> styling hanya berlaku untuk komponen ini saja

Pada Vue disebut istilah SFC (single file component), semua dalam satu komponen script, template, style

<input v-model="newTask" type="text" name="newTask">

v-model -->  data pada variabel newTask akan terhubung langsung (two-way) ke input teks ini


