<script setup>

import { watch } from 'vue';
import { useRoute } from 'vue-router';
import NavbarComponent from './components/NavbarComponent.vue';
const route = useRoute();

watch(
  () => route.fullPath,
  () => {
    document.title = String(route.meta?.title || route.name || 'App');
  },
  { immediate: true }
);
</script>

<template>
    <RouterView class="py-24 px-6 lg:w-3/7 mx-auto relative z-20" />
    <NavbarComponent/>

  <span class="select-none flex fixed top-5 left-5 z-50 bg-white/50  font-mono lg:top-0 lg:bottom-5 lg:top-auto p-1">
    <a v-for="part in ['/home', ...route.path.split('/').filter(Boolean)]" :key="part">{{ part }}/</a>
  </span>

</template>
