<template>
  <div class="grid place-content-center h-screen">
    <h1 class="text-9xl">{{ timestamp }}</h1>
  </div>
</template>

<script setup >
const timestamp = ref(Date.now());
let intervalId;
onMounted(() => {
  intervalId = setInterval(() => {
    timestamp.value = Date.now();
  }, 1);
});
onUnmounted(() => {
  clearInterval(intervalId);
});
</script>