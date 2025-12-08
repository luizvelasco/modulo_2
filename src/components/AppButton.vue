<template>
    <button @click="onClick"
        :class="{'active': props.variant === 'active', 
        'inactive': props.variant === 'inactive'

        }"
    >
        <slot>Click Me</slot>
        ({{ clicks }})
    </button>

</template>

<script setup>
import { ref } from 'vue';

    const props = defineProps(['variant']);

    const clicks = ref(0);
    const onClick = () => {
        clicks.value += 1;
    };
</script>

<style>
    .active {
        background-color: green;
        color: white;
    }
    .inactive {
        background-color: red;
        color: white;
    }   
</style>