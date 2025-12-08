<script setup>
import { ref } from 'vue';
import AppButton from './components/AppButton.vue';
const totalClicks = ref(0);
const changeCount = () => {
  totalClicks.value++;
};

</script>

<template>
  <div>
    Total de cliques: {{ totalClicks }} <br><br>
   <AppButton variant="active" @contador-mudou="changeCount">Salvar</AppButton><br>
   <AppButton variant="inactive" @contador-mudou="changeCount">Deletar</AppButton><br>
  </div>
</template>