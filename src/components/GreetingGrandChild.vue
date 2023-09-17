<template>
  <div class="box">
    <span>Grand Child Component</span>
    <h1>{{ parentMessage }}</h1>
  </div>
</template>

<script setup>
  import { inject } from 'vue';
  /* Catch the provide data from grand parent component */
  const parentMessage = inject('parentMessage');
</script>
  