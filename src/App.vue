<template>
  <div style="text-align: center">
    <img alt="Vue logo" src="./assets/logo.png" />
    <div style="margin: auto; width: 300px; text-align: center">
      <a-typography-text v-model:content="editableStr" :editable="{ onCancel: handleCancel, onEnd: handleEnd }" />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const editableStr = ref('a-typography-text bug')
const handleCancel = () => {
  console.log('handleCancel')
}
const handleEnd = () => {
  console.log('handleEnd')
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
