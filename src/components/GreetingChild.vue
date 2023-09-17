<template>
  <h1>{{ parentMessage }}</h1>
  <p>Child Component</p>
  <GreetingGrandChild></GreetingGrandChild>
</template>
<script setup>
import { inject } from 'vue';
import GreetingGrandChild from './GreetingGrandChild.vue';
/* Catch the provide data from parent component */
const parentMessage = inject('parentMessage');
</script>
  