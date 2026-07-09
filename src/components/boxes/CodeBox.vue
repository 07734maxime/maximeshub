<script setup>
defineProps({
  lang: { type: String, default: 'rust' },
  code: { type: String, required: true }
});
</script>

<template>
  <div class="select-none flex flex-col solid-shadow-3 rounded-lg bg-black">
    <ul class="flex gap-1 bg-neutral-900 rounded-t-lg py-1 px-2">
      <li><i class="fas fa-circle text-red-400"></i></li>
      <li><i class="fas fa-circle text-orange-400"></i></li>
      <li><i class="fas fa-circle text-green-400"></i></li>
    </ul>
    <CodeBlock :language="lang" :code="code" />
  </div>
</template>

<script>
import CodeBlock from '@/components/CodeBlock.vue';
export default { components: { CodeBlock } };
</script>