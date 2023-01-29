<template>
  <section class="home__hero">
    <nav>
      <h3>NILES</h3>
      <ul :class="{ active: active }">
        <li @click="active = !active">
          <a href="#about">ABOUT</a>
        </li>
        <li @click="active = !active">
          <a href="#works">WORKS</a>
        </li>
        <li @click="active = !active">
          <a href="#contact">CONTACT</a>
        </li>
      </ul>
      <div class="toggle" @click="active = !active">
        <div class="box"></div>
        <div class="box"></div>
        <div class="box"></div>
      </div>
    </nav>
    <div class="home__hero__content">
      <div class="text">
        <h4
          data-aos="fade-up"
          data-aos-duration="500"
          data-aos-easing="linear"
          data-aos-delay="100"
        >
          It’s empty<br />
          in here,<br />
          isn’t it?
        </h4>
        <p
          data-aos="fade-up"
          data-aos-duration="500"
          data-aos-easing="linear"
          data-aos-delay="200"
        >
          I am a solution-oriented developer who is dedicated to creating and
          optimizing interactive, user- friendly, and feature-rich web
          applications to solve everyday problems.
        </p>
      </div>
      <img
        src="@/assets/geek.gif"
        alt="A hero image"
        width="853"
        height="853"
      />
      <!-- <video width="853" height="853">
        <source src="@/assets/geek.gif" type="video/gif" />
      </video> -->
    </div>
  </section>
</template>

<script setup>
import { onMounted, ref } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";
onMounted(() => {
  AOS.init();
});
const active = ref(false);
</script>

<style scoped lang="scss">
@import "./home.scss";
</style>
