<script setup>
import { useRoute } from 'vue-router';
import { onMounted, ref } from 'vue';
import AboutBox from '@/components/boxes/AboutBox.vue';
const route = useRoute();

const layout = ref('hiragana');
const switchLayout = (newLayout) => { layout.value = newLayout; };

const rows = [
  [{ hiragana: 'あ', katakana: 'ア', romaji: 'a' }, { hiragana: 'い', katakana: 'イ', romaji: 'i' }, { hiragana: 'う', katakana: 'ウ', romaji: 'u' }, { hiragana: 'え', katakana: 'エ', romaji: 'e' }, { hiragana: 'お', katakana: 'オ', romaji: 'o' }],
  [{ hiragana: 'か', katakana: 'カ', romaji: 'ka' }, { hiragana: 'き', katakana: 'キ', romaji: 'ki' }, { hiragana: 'く', katakana: 'ク', romaji: 'ku' }, { hiragana: 'け', katakana: 'ケ', romaji: 'ke' }, { hiragana: 'こ', katakana: 'コ', romaji: 'ko' }],
  [{ hiragana: 'さ', katakana: 'サ', romaji: 'sa' }, { hiragana: 'し', katakana: 'シ', romaji: 'shi' }, { hiragana: 'す', katakana: 'ス', romaji: 'su' }, { hiragana: 'せ', katakana: 'セ', romaji: 'se' }, { hiragana: 'そ', katakana: 'ソ', romaji: 'so' }],
  [{ hiragana: 'た', katakana: 'タ', romaji: 'ta' }, { hiragana: 'ち', katakana: 'チ', romaji: 'chi' }, { hiragana: 'つ', katakana: 'ツ', romaji: 'tsu' }, { hiragana: 'て', katakana: 'テ', romaji: 'te' }, { hiragana: 'と', katakana: 'ト', romaji: 'to' }],
  [{ hiragana: 'な', katakana: 'ナ', romaji: 'na' }, { hiragana: 'に', katakana: 'ニ', romaji: 'ni' }, { hiragana: 'ぬ', katakana: 'ヌ', romaji: 'nu' }, { hiragana: 'ね', katakana: 'ネ', romaji: 'ne' }, { hiragana: 'の', katakana: 'ノ', romaji: 'no' }],
  [{ hiragana: 'は', katakana: 'ハ', romaji: 'ha' }, { hiragana: 'ひ', katakana: 'ヒ', romaji: 'hi' }, { hiragana: 'ふ', katakana: 'フ', romaji: 'fu' }, { hiragana: 'へ', katakana: 'ヘ', romaji: 'he' }, { hiragana: 'ほ', katakana: 'ホ', romaji: 'ho' }],
  [{ hiragana: 'ま', katakana: 'マ', romaji: 'ma' }, { hiragana: 'み', katakana: 'ミ', romaji: 'mi' }, { hiragana: 'む', katakana: 'ム', romaji: 'mu' }, { hiragana: 'め', katakana: 'メ', romaji: 'me' }, { hiragana: 'も', katakana: 'モ', romaji: 'mo' }],
  [{ hiragana: 'や', katakana: 'ヤ', romaji: 'ya' }, null, { hiragana: 'ゆ', katakana: 'ユ', romaji: 'yu' }, null, { hiragana: 'よ', katakana: 'ヨ', romaji: 'yo' }],
  [{ hiragana: 'ら', katakana: 'ラ', romaji: 'ra' }, { hiragana: 'り', katakana: 'リ', romaji: 'ri' }, { hiragana: 'る', katakana: 'ル', romaji: 'ru' }, { hiragana: 'れ', katakana: 'レ', romaji: 're' }, { hiragana: 'ろ', katakana: 'ロ', romaji: 'ro' }],
  [{ hiragana: 'わ', katakana: 'ワ', romaji: 'wa' }, null, null, null, { hiragana: 'を', katakana: 'ヲ', romaji: 'wo' }],
  [{ hiragana: 'ん', katakana: 'ン', romaji: 'n' }, null, null, null, null],
];

const alphabet = rows.flat();

const playKana = (char) => {
  if (!char) return;
  const audio = new Audio(`/audio/${char.romaji}.mp3`);
  audio.play();
};
</script>

<template>
  <main class="flex flex-col gap-3">
    <h1 class="highlight-title text-3xl -rotate-1">{{ route.name }}</h1>
    <AboutBox>Tap on a card to hear a character pronunciation.</AboutBox>

    <div class="flex gap-2">
      <button :class="layout === 'hiragana' ? 'bg-orange-300' : 'bg-purple-200 opacity-50'"
        class="font-bold text-sm uppercase border border-2 p-2 rounded flex-1 cursor-pointer"
        @click="switchLayout('hiragana')">あ Hiragana</button>
      <button :class="layout === 'katakana' ? 'bg-orange-300' : 'bg-purple-200 opacity-50'"
        class="font-bold text-sm uppercase border border-2 p-2 rounded flex-1 cursor-pointer"
        @click="switchLayout('katakana')">ア Katakana</button>
    </div>

    <ul class="grid grid-cols-5 gap-5 text-xl">
      <li v-for="(char, index) in alphabet" :key="index"
          :class="char ? 'solid-shadow-3 select-none cursor-pointer bg-white p-2 border border-2' : ''"
          class="p-4 text-center flex flex-col items-center justify-center gap-1.5"
          @click="playKana(char)">
        <template v-if="char">
          <span class="font-bold text-2xl">{{ char[layout] }}</span>
          <span class="italic text-gray-600 text-sm">{{ char.romaji }}</span>
          <i class="text-gray-600 text-sm fas fa-volume-up"></i>
        </template>
      </li>
    </ul>
  </main>
</template>