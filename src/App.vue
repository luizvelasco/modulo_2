<script setup>
  import { computed, ref } from 'vue';

  const user = ref ({
    first_name: 'Jon',
    last_name: 'Snow'
  })

  const fullName = computed(() => {
    return `${user.value.first_name} ${user.value.last_name}`
  })
</script>

<template>
  <div>
    {{ user.first_name }} {{ user.last_name }} <br>
    {{ fullName }}
  </div>
</template>