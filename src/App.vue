<script setup>
  import { computed, ref } from 'vue';

  const users = ref ([
    {name: 'Rebeca', age: 15},
    {name: 'Jon', age: 20},
    {name: 'Maria', age: 50},
  ])

  const adults = computed(() => {
    return users.value.filter(user => user.age >= 18);
  })

</script>

<template>
  <div>
    <ul>
      <li v-for="user in adults" :key="user.name">
        {{ user.name }}
      </li>
    </ul>
   
  </div>
</template>