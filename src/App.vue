<script setup>
  import { computed, ref } from 'vue';

  const products = ref ([
    {name: 'Iphone', price: 100},
    {name: 'Macbook', price: 500},
  ])

  const total = computed(() => {
    return products.value.reduce((sum, product) => sum + product.price, 0);
  })
</script>

<template>
  <div>
    {{ total }}
  </div>
</template>