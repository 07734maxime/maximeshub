<script setup>
import HomeContent from '../components/HomeContent.vue'
</script>

<template>
  <main>
    <HomeContent />
      <section>
      <h2>Navigation</h2>
        <ul>
          <li><RouterLink to="/projects">Projects</RouterLink></li>
          <li><RouterLink to="/hobbies">Hobbies</RouterLink></li>
          <li><RouterLink to="/blog">Blog</RouterLink></li>
        </ul>
  </section>
  <section>
        <h2>Contact</h2>
        <p>Despite not being active on social media, here are ways to get in touch:</p>
        <ul>
          <li><a href="mailto:e07734maxime@proton.me">Mail-me</a></li>
          <li><a target="_blank" rel="noopener noreferrer" href="https://github.com/32418354892175849324308957643254">GitHub</a></li>
          <li><a target="_blank" rel="noopener noreferrer" href="https://discord.com/users/680737784730091522">Discord</a></li>
        </ul>
  </section>
  </main>
</template>
