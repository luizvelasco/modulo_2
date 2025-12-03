<script setup>
import { ref } from 'vue';
const title = ref('Hello World 3');
const showTitle = ref(true);
</script>

<template>
  <div>
    <h1 v-if="showTitle">{{ title }}</h1>
  </div>
</template>
