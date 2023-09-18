<template>
  <div class="box">
    <span>Parent Component</span>
    <h1>{{ parentMessage }}</h1>
    <!-- Included Child Component -->
    <GreetingChild />
  </div>
</template> 
<script setup>
  import { inject } from 'vue'
  import GreetingChild from './GreetingChild.vue'
  const parentMessage = inject('parentMessage')
</script>
  