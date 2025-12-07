<script setup>
  import { watch, ref } from 'vue';
  const name = ref('');
  
  watch(name, (newValue, oldValue) => {
    console.log(newValue)
    
  });

</script>

<template>
  <div>
   <input type="text" v-model="name">
  </div>
</template>