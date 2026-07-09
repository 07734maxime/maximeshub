<script setup>
defineProps({
  label: { type: String, default: 'LaTeX' }
});
</script>

<template>
  <div class="relative bg-white p-1 border border-2 solid-shadow-3 rounded">
    <Latex :displayMode="true"><slot /></Latex>
    <p class="text-sm text-gray-500/50 m-2 absolute bottom-0 right-0">{{ label }}</p>
  </div>
</template>

<script>
import Latex from '@/components/Latex.vue';
export default { components: { Latex } };
</script>