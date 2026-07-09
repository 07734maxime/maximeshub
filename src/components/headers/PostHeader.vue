<script setup>
import { useRoute } from 'vue-router';
const route = useRoute();
</script>

<template>
  <hgroup class="flex flex-col gap-2">
    <h1 class="highlight-title text-center text-xl">{{ route.name }}</h1>
    <ul class="flex gap-2">
      <li v-for="(tag, index) in route.meta.tags" :key="index"
          class="select-none cursor-pointer border border-black border-2 text-white bg-gray-200 text-gray-800 text-xs px-2 py-1 uppercase font-mono font-bold"
          :class="tag.color">
        <span class="highlight-tag">{{ tag.label }}</span>
      </li>
    </ul>
  </hgroup>
</template>