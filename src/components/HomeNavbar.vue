<script setup lang="ts">
  import PrimeMenubar from 'primevue/menubar';
  import { computed } from 'vue';
  const props = defineProps<{ items: string[] }>();

  const mapItemsToModel = computed(() => {
    const model = [];

    for (let item of props.items) {
      model.push({ label: item });
    }

    return model;
  });
</script>

<template>
  <PrimeMenubar :model="mapItemsToModel" />
</template>
