<template>
  <span>Child Component</span>
  <h1>{{ greeting }}</h1>
  <GreetingGrandChild :greeting="greeting"></GreetingGrandChild>
</template>
<script setup>
import { inject } from 'vue';
import GreetingGrandChild from './GreetingGrandChild.vue';
/* Catch the provide data from parent component */
const parentMessage = inject('parentMessage');

const props = defineProps({
  greeting:String
})
</script>
  