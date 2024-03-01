<template>
  <div>
    <p
      class="text-7xl grid place-content-center h-screen dark:bg-neutral-900 dark:text-neutral-50"
    >
      {{ date }}
    </p>
  </div>
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
