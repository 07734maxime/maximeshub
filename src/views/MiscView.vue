<script setup>
import AboutBox from '@/components/boxes/AboutBox.vue';
import { ref } from 'vue';
import { useRouter, useRoute } from 'vue-router';
const router = useRouter();
const miscRoutes = ref(router.getRoutes().filter(route => route.path.startsWith("/misc/")));

const route = useRoute();

</script>

<template>
  <main class="flex flex-col gap-4">
    <h1 class="highlight-title rotate-2 text-3xl">{{ route.name }}</h1>

    <AboutBox>
        Stuff related to other pages, that are not referenced in the main navigation. Might add other things later.
    </AboutBox>

    <section class="flex flex-col gap-3">
      <h2 class="text-xl highlight-title -rotate-1">Navigation</h2>
      <ul class="flex flex-col gap-2 list-none p-0">

        <li v-for="route in miscRoutes" :key="route.path" :to="route.path"
          class="bg-purple-300 p-2 border border-2 rounded-tr rounded-bl flex flex-col gap-3 solid-shadow-3">

          <div class="flex justify-between items-center">
            <span class="font-bold font-mono">{{ route.name }}</span>
            <RouterLink :to="route.path"
              class="bg-black p-2 text-white hover:bg-gray-700 w-fit ml-auto font-mono text-sm">Go <i
                class="fas fa-arrow-right"></i></RouterLink>
          </div>
        </li>

      </ul>
    </section>

    <p class="font-mono text-sm text-gray-600">
      FYI. This website is still under construction. <a class="highlight-link" href="https://github.com/KaTeX/KaTeX"
        target="_blank" rel="noopener noreferrer">KaTeX</a> was used for mathematical typesetting. I also do not own the
      rights to any images used. <a class="highlight-link" href="mailto:07734maxime@proton.me" target="_blank"
        rel="noopener noreferrer">Contact me</a> for any content removal requests.
    </p>

  </main>
</template>