<template>
  <h1>App Component</h1>
  <!-- Counter sample  -->
  <Counter/>
  <!-- Included Parent component-->
  <GreetingParent />
</template>

<script setup>
  import { provide,ref } from 'vue'
  import Counter from './components/Counter.vue'
  import GreetingParent from './components/GreetingParent.vue'
  const parentMessage = ref('Greeting from app.vue')
  /* Provide used for the direct data pass to grand child */
  provide('parentMessage', parentMessage)
</script>
