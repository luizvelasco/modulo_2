<script setup>
  import { ref } from 'vue';
  const counter = ref(0);
  const onClick = () => {
    counter.value ++;
  }

  const onFocus = () => {
    console.log('onFocus');
  }

  const onMouseover = () => {
    console.log('onMouseover');
    
  }

</script>

<template>
  <div>
    Contador: {{ counter }}
    <button @click="onClick">
      Click
    </button>

    <br>

    <input type="text" @focus="onFocus" @mouseover="onMouseover">
  </div>
</template>