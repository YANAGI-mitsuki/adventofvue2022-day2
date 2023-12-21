<script setup>
import { ref } from "vue";
const buttonText = ref('tell me!');
const changeButtonText = () => {
  buttonText.value = 'another';
};
const jokes = ref([
  {
    id: 1,
    content: '布団が',
    selected: true
  },
  {
    id: 2,
    content: '吹っ飛んだ',
    selected: false
  }
])
// const changeText = () => {
//   jokes[0].content = '吹っ飛んだ'
// };
const text = ref()
const changeText = () => {
  text.value = '吹っ飛んだ'
};

</script>

<template>
<div id="app">
  <!-- <button @click="changeButtonText">{{ buttonText }}</button> -->
  <!-- <button @click="changeText">tell me!</button>
  <p v-if="jokes[0].selected">{{ jokes[0].content }}</p> -->
  <button @click="changeText">tell me!</button>
  <p v-if="jokes[0].selected">{{ jokes[0].content }}</p>
  <p v-if="jokes[0].selected">{{ text }}</p>
  <!-- <button @click="jokes[0].selected=!jokes[0].selected">tell me!</button><br/> -->
  <!-- <button @click="jokes[1].selected=!jokes[1].selected">another</button><br/> -->
  <!-- <p v-if="jokes[1].selected">{{ jokes[1].content }}</p> -->
</div>
</template>

<style scoped>

</style>
