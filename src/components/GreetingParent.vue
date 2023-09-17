<template>
  <span>Parent Component</span>
  <h1>{{ message }}</h1>
  <!-- Included Child Component -->
  <GreetingChild :greeting="message" />
</template> 
<script setup>
/* Provide also known as props drilling means dirent to pass data to grand child */
import { provide } from 'vue';
import GreetingChild from './GreetingChild.vue';
/* Defined props here */
const props = defineProps({
  message: String,
})
const parentMessage = 'Greeting from GreetingParent.vue'
provide('parentMessage', parentMessage);

</script>
  