<script setup>
import { ref } from 'vue';

const model = defineModel();
</script>

<template>
  <div>
    <input type="text" v-model="model">
  </div>
</template>
