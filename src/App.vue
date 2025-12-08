<script setup>
import { ref } from 'vue';
import AppButton from './components/AppButton.vue';

</script>

<template>
  <div>
   <AppButton variant="active">Salvar</AppButton><br>
   <AppButton variant="inactive">Deletar</AppButton><br>
  </div>
</template>