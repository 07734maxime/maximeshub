<template>
  <main class="flex flex-col gap-3">
    <PostHeader />

    <AboutBox>
        <i class="fa fa-solid fa-triangle-exclamation"></i> You will need to have suitable fonts installed to properly display Japanese characters.
    </AboutBox>

    <p class="font-mono">From a simple idea to a concrete project, I will relate my path of learning Japanese.
      Thankfully I've always had ease to learn languages, but I've never used my potential except for English.
      This combined with my interest with Japanese culture made me start learning the lang.
    </p>

    <SectionTitle>Context</SectionTitle>

    <p class="font-mono">My plan started when I was 15.I basically gave up really really fast, even though
      I haven't forgotten this idea. 5 years later, I've really started learning Japanese.
    </p>

    <p class="font-mono">How this language is structured ? Basically, Japanese uses 3 differents writing systems :</p>

    <div class="bg-purple-300 p-2 border border-2 solid-shadow-3 flex flex-col gap-2">
        <span class="font-mono">The 3 writing systems</span>
                <ul class="flex justify-around gap-2 ">
          <li class="flex-1 bg-white border border-2 p-2 items-center justify-center flex font-mono flex-col">
                <span>ひらがな</span>
                <span class="text-xs text-gray-500">Hiragana</span>
            </li>
          <li class="flex-1 bg-white border border-2 p-2 items-center justify-center flex font-mono flex-col">
                <span>カタカナ</span>
                <span class="text-xs text-gray-500">Katakana</span>
            </li>
          <li class="flex-1 bg-white border border-2 p-2 items-center justify-center flex font-mono flex-col">
                <span>漢字</span>
                <span class="text-xs text-gray-500">Kanji</span>
            </li>
        </ul>
    </div>

    


    <p class="font-mono">
      Hiragana and Katakana are both made of 46 basic characters, and share the same sounds.
      The difference is that Hiragana is used for native Japanese words, while Katakana is used for foreign words.
      Kanji, on the other hand, are Chinese characters that have been adopted into the Japanese writing system.
    </p>

    <div class="bg-white border-2 border-black p-3 solid-shadow-3 overflow-x-auto font-mono">
        <table class="w-full border-collapse text-center text-sm">
            <thead>
                <tr class="border-b-2 border-black">
                    <th class="p-1.5"></th>
                    <th class="p-1.5">a</th>
                    <th class="p-1.5">i</th>
                    <th class="p-1.5">u</th>
                    <th class="p-1.5">e</th>
                    <th class="p-1.5">o</th>
                </tr>
            </thead>
            <tbody>
                <tr class="border-b border-gray-200">
                    <th class="p-1.5 text-left font-bold">Hiragana</th>
                    <td class="p-1.5">あ</td>
                    <td class="p-1.5">い</td>
                    <td class="p-1.5">う</td>
                    <td class="p-1.5">え</td>
                    <td class="p-1.5">お</td>
                </tr>
                <tr class="border-b border-gray-200">
                    <th class="p-1.5 text-left font-bold">Katakana</th>
                    <td class="p-1.5">ア</td>
                    <td class="p-1.5">イ</td>
                    <td class="p-1.5">ウ</td>
                    <td class="p-1.5">エ</td>
                    <td class="p-1.5">オ</td>
                </tr>
                <tr>
                    <th class="p-1.5 text-left font-bold">Romaji</th>
                    <td class="p-1.5">a</td>
                    <td class="p-1.5">i</td>
                    <td class="p-1.5">u</td>
                    <td class="p-1.5">e</td>
                    <td class="p-1.5">o</td>
                </tr>
            </tbody>
        </table>
    </div>

    <AboutBox>
      <p>I've created a page so you can explore the full Japanese alphabet. If you want to learn more,
      <RouterLink class="highlight-link" to="/stuff/japanese-alphabet">click here</RouterLink></p>
    </AboutBox>

    <SectionTitle>How is learning Japanese?</SectionTitle>

    <p class="font-mono">In <a href="https://www.youtube.com/watch?v=tkFOBx6j0l8" target="_blank" class="hover:underline italic no-underline text-black">two words</a>: really hard.</p>

    <p class="font-mono">Unironically, what makes Japanese hard is not even the writing system. It's very easy to learn. Same grammar,
      it's also not that complicated. They use a SOV (Subject-Object-Verb) system.
      What makes Japanse really, really difficult is vocabulary : there's no latin roots to lean on.
    </p>

    <p class="font-mono">When you learn Japanese, there is something called <a href="https://www.jlpt.jp/" target="_blank">Japanese-Language Proficiency Test</a>, also called <span class="italic"> JLPT </span>.
      It's basically a test to measure your Japanese language skills, as a foreigner. This test is divided into several levels, starting from N5 (beginner) to N1 (advanced).
    </p>

    <div class="bg-white border-2 border-red-500 p-3 solid-shadow-3 flex flex-col gap-1< font-mono">
      <span>JLPT progress</span>
      <p class="text-sm text-gray-600">Currently preparing for <span class="text-red-600">N5</span>. Going well before my break - first time learning something this slowly.</p>
    </div>

    <SectionTitle>Let's talk about Kanji</SectionTitle>

    <p class="font-mono">Kanji are used to represent ideas and concepts, rather than sounds.
      This means that each Kanji character has a specific meaning, and you have to learn both the reading and the meaning of each character.
      Also, there is two readings for each Kanji character, the <span class="italic">On'yomi</span> (<span class="font-bold">音読み</span>) and the <span class="italic">Kun'yomi</span> (<span class="font-bold"> 訓読み</span>).
      On'yomi is the reading of the Kanji character when it is used in a compound word, while Kun'yomi is the reading of the Kanji character when it is used alone.
      If you don't understand how can Kanji be useful, I'll show you a pretty simple example:
    </p>
    <ul class="flex flex-col gap-2">
      <li class="bg-white justify-between p-2 border border-2 flex gap-1 items-center solid-shadow-3">
        <span class="text-center text-3xl">知</span>
        <p>(shi) - represents the concept of "knowing"</p>
      </li>
      <li class="bg-white justify-between p-2 border border-2 flex gap-1 items-center solid-shadow-3">
        <span class="text-center text-3xl">死</span>
        <p>(shi) - represents the concept of "death"</p>
      </li>
    </ul>

    <SectionTitle>Japanese Grammar</SectionTitle>

    <p class="font-mono">
      Japanese grammar is actually not that hard once you get the hang of it. It's all bout understanding the SOV system,
      and how to "conjugate" verbs. I think the best thing to do is to train
      regularly, and try to understand the logic behind all that instead of rote memorizing.
    </p>

    <SectionTitle>What I've Learned</SectionTitle>
    <UncompleteBox>More coming soon...</UncompleteBox>
  </main>
</template>

<script setup>
import AboutBox from '@/components/boxes/AboutBox.vue';
import PostHeader from '@/components/headers/PostHeader.vue';
import SectionTitle from '@/components/SectionTitle.vue';
import UncompleteBox from '@/components/boxes/UncompleteBox.vue';
</script>