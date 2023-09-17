<template>
  <div>
    <span>Grand Child Component</span>
    <h1>{{ greeting }}</h1>
  </div>
</template>

<script setup>
  import { inject } from 'vue';
  /* Catch the provide data from grand parent component */
  const parentMessage = inject('parentMessage');
  const props = defineProps({
    greeting:String
  })
</script>
  