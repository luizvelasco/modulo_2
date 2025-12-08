<script setup>
import { ref } from 'vue';
import AppInput from './components/AppInput.vue';
const name = ref('');
const sobrenome = ref('');

</script>

<template>
  <div>
    {{ name }} <br>
    <AppInput v-model="name"/>
  </div>

  <div>
    {{ sobrenome }} <br>
    <AppInput v-model="sobrenome"/>
  </div>

</template>