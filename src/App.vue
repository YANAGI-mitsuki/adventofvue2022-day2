<script setup>
import { ref } from "vue";
const jokes = ref([
  {
    id: 1,
    content: '布団が',
    selected: false
  },
  {
    id: 2,
    content: '吹っ飛んだ',
    selected: false
  }
])
</script>

<template>
<div id="app">
  <button @click="jokes[0].selected=!jokes[0].selected">tell me!</button><br/>
  <p v-if="jokes[0].selected">{{ jokes[0].content }}</p>
  <button @click="jokes[1].selected=!jokes[1].selected">another</button><br/>
  <p v-if="jokes[1].selected">{{ jokes[1].content }}</p>
</div>
</template>

<style scoped>

</style>
