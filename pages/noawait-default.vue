<script setup lang="ts">
const asyncData = useAsyncData(
  () =>
    new Promise((resolve) => {
      setTimeout(() => resolve("data"), 4000);
    })
);

const asyncData1 = useAsyncData(
  () =>
    new Promise((resolve) => {
      setTimeout(() => resolve("data"), 4000);
    })
);
</script>

<template>
  <div>
    {{ asyncData.data.value ?? "Loading..." }}
    {{ asyncData1.data.value ?? "Loading..." }}
  </div>
</template>
