<script setup>
defineProps({
  title: { type: String, required: true }
});
</script>

<template>
  <li class="solid-shadow-3 flex flex-col p-2 bg-white border border-2 rounded-tl rounded-br">
    <span class="font-mono flex flex-col text-center">
      {{ title }} <slot name="formula" />
    </span>
    <span>
      <slot name="result" />
    </span>
  </li>
</template>