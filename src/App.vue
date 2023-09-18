<template>
  <h1>App Component</h1>
  <!-- Count sample  -->
  <p>Count: {{ count }}</p>
  <button @click="count++">Increment Count</button>
  <!-- Included Parent component-->
  <GreetingParent />
</template>

<script setup>
import { provide,ref } from 'vue';
import {  } from 'vue';
import GreetingParent from './components/GreetingParent.vue';
  const count = ref(0);
  const parentMessage = 'Greeting from app.vue'
  /* Provide used for the direct data pass to grand child */
  provide('parentMessage', parentMessage);
</script>
