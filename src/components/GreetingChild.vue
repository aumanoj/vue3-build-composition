<template>
  <div class="box">
  <span>Child Component</span>
  <h1>{{ parentMessage }}</h1>
  <GreetingGrandChild></GreetingGrandChild>
</div>
</template>
<script setup>
import { inject } from 'vue';
import GreetingGrandChild from './GreetingGrandChild.vue';
/* Catch the provide data from parent component */
const parentMessage = inject('parentMessage');
</script>
  