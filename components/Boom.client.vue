<script setup lang="ts">
const loading = ref(true);

if (process.client) {
  setTimeout(() => {
    loading.value = false;
  }, 1500);
}
</script>

<template>
  <div>BOOM</div>
  <div v-show="loading">
    <slot name="test" />
  </div>
</template>
