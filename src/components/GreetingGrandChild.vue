<template>
  <div>
    <h1>{{ parentMessage }}</h1>
    <p>Grand Child Component</p>
  </div>
</template>

<script setup>
  import { inject } from 'vue';
  /* Catch the provide data from grand parent component */
  const parentMessage = inject('parentMessage');
</script>
  