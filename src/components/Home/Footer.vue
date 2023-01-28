<template>
  <section class="home__footer" id="contact">
    <div class="text">
      <h2>open to projects & collaborations</h2>
      <p>
        contact forms ain’t my thing, just shoot a mail - i’ll be replying your
        mail as fast as the Expansion of the Universe
      </p>
      <a href="mailto:egbaidomehjamez@gmail.com"
        ><button>SHOOT ME A MAIL</button></a
      >
    </div>
    <h3 class="cursive">hello world, i’m Niles, and i’m amazing!</h3>
    <footer>
      <ul>
        <li v-for="item in links" :key="item.id">
          <a :href="item.link" target="__blank">{{ item.title }}</a>
        </li>
      </ul>
      <a href="mailto:egbaidomehjamez@gmail.com" target="__blank"
        >hello@niles.dev</a
      >
      <p>© 2023 James Egbaidomeh. All rights reserved.</p>
    </footer>
  </section>
</template>

<script setup>
import { ref } from "vue";
const links = ref([
  {
    id: 1,
    title: "GitHub",
    link: "https://github.com/nilesjamex",
  },
  {
    id: 2,
    title: "LinkedIn",
    link: "https://www.linkedin.com/in/jamesegbaidomeh",
  },
  {
    id: 3,
    title: "Twitter",
    link: "https://twitter.com/0x9nn",
  },
]);
</script>

<style scoped lang="scss">
@import "./home.scss";
</style>
