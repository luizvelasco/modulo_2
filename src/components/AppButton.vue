<script setup>
import { ref } from 'vue';

    const clicks = ref(0);
    const onClick = () => {
        clicks.value += 1;
    };
</script>

<template>
    <button @click="onClick">
        <slot>Click Me</slot>
        ({{ clicks }})
    </button>

</template>

