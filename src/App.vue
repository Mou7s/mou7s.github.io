<template>
    {{ date }}
</template>

<script setup>
import { ref, onUnmounted } from 'vue';

const date = ref(Date.now());

const intervalId = setInterval(() => {
    date.value = Date.now();
}, 1);

onUnmounted(() => {
    clearInterval(intervalId);
});
</script>