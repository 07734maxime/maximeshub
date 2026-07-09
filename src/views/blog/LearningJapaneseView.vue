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

    <p>My plan started when I was 15.I basically gave up really really fast, even though
      I haven't forgotten this idea. 5 years later, I've really started learning Japanese.
    </p>

    <p>How this language is structured ? Basically, Japanese uses 3 differents writing systems :</p>

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

    


    <p>
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
        <i class="fas fa-book-open"></i>
      I've created a page so you can explore the full Japanese alphabet. If you want to learn more,
      <RouterLink class="highlight-link" to="/stuff/japanese-alphabet">click here</RouterLink>
    </AboutBox>

    <SectionTitle>How is learning Japanese?</SectionTitle>

    <p>In <a href="https://www.youtube.com/watch?v=tkFOBx6j0l8" target="_blank" class="hover:underline italic no-underline text-black">two words</a>: really hard.</p>

    <p>Unironically, what makes Japanese hard is not even the writing system. It's very easy to learn, and pronunciation is really straightforward, even a 2-year-old can learn it.
      Japanese grammar is also not that complicated, it's basically a SOV system : subject-object-verb. It can be complex the first time when you always used a SVO system as I,
      but it's not that tough to get used to it. What makes Japanse really, really difficult is vocabulary.
    </p>

    <p>
      As a latin-language speaker, all the words you know are based on Latin roots,
      and you can easily deduce the meaning of a word you don't know by looking at its root.
      In Japanese, there is no such thing, and you have to learn every single word by heart. This is really frustrating because this makes you stuck at the simple sentences,
      and you can't really express yourself in a complex way.
    </p>

    <hr class="my-6" />

    <p>When you learn Japanese, there is something called <a href="https://www.jlpt.jp/" target="_blank">Japanese-Language Proficiency Test</a>, also called <span class="italic"> JLPT </span>.
      It's basically a test to measure your Japanese language skills, as a foreigner. This test is divided into several levels, starting from N5 (beginner) to N1 (advanced).
      <span class="text-red-600">Currently, I'm preparing for the JLPT N5.</span> I'd say before my break, it was going well, but this is the first time
      that I'm really slow to learn something.</p>

    <SectionTitle>Let's talk about Kanji</SectionTitle>

    <p>As said previously, Kanji are used to represent ideas and concepts, rather than sounds.
      This means that each Kanji character has a specific meaning, and you have to learn both the reading and the meaning of each character.
      Also, there is two readings for each Kanji character, the <span class="italic">On'yomi</span> (<span class="font-bold">音読み</span>) and the <span class="italic">Kun'yomi</span> (<span class="font-bold"> 訓読み</span>).
      On'yomi is the reading of the Kanji character when it is used in a compound word, while Kun'yomi is the reading of the Kanji character when it is used alone.
      If you don't understand how can Kanji be useful, I'll show you a pretty simple example:
    </p>
    <ul>
      <li><span class="font-bold">知らない</span> (<span class="italic">shiranai</span>) literally means "I don't know". Here, the <span class="font-bold">知</span> Kanji represents the concept of "knowing", so context can be deduced easily with this one.</li>
      <li><span class="font-bold">死</span> (<span class="italic">shi</span>) literally means "death". Here, the <span class="font-bold">死</span> Kanji represents the concept of "death", so context can be deduced easily with this one.</li>
    </ul>
    <p>As you may have noticed, Japanese have a lot of common sounds for different words, different meanings, so Kanji are there to represent the different meaning through an image, an idea to exactly deduce the context of the conversation.</p>

    <SectionTitle>Japanese Grammar</SectionTitle>

    <p>
      Japanese grammar is actually not that hard once you get the hang of it. As said earlier,
      it's all bout understanding the SOV system, and how to "conjugate" verbs (because this is reammy easy). I think the best thing to do is to train
      regularly, and try to understand the logic behind all that instead of learning by heart.
    </p>

    <SectionTitle>What I've Learned</SectionTitle>
    <p>To be continued...</p>
  </main>
</template>

<script setup>
import AboutBox from '@/components/boxes/AboutBox.vue';
import PostHeader from '@/components/headers/PostHeader.vue';
import SectionTitle from '@/components/SectionTitle.vue';
</script>