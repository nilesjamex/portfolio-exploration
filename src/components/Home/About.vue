<template>
  <section class="home__about" id="about">
    <h4
      data-aos="fade-up"
      data-aos-duration="500"
      data-aos-easing="linear"
      data-aos-delay="100"
    >
      About
    </h4>
    <p
      data-aos="fade-up"
      data-aos-duration="500"
      data-aos-easing="linear"
      data-aos-delay="200"
    >
      I am a software developer based in Ibadan, Nigeria with a passion for
      crafting visually stunning and interactive digital experiences. My
      expertise lies in CSS, animation, and user interaction design, and I am
      always striving to improve my skills and push the boundaries of what is
      possible. As a developer, I find great satisfaction in simplifying complex
      code and making it more efficient, and I am always on the lookout for new
      and innovative ways to solve problems.
    </p>
    <span
      data-aos="fade-up"
      data-aos-duration="500"
      data-aos-easing="linear"
      data-aos-delay="300"
    >
      <a
        href="https://docs.google.com/document/d/1Si2w1XLd2gUo0zMIc-HIehSjFU-IdXY6DHfCcz4f0_U/edit?usp=share_link"
        target="__blank"
      >
        Link to my resume
        <img src="@/assets/arrow.svg" alt="" />
      </a>
    </span>
    <h4
      data-aos="fade-up"
      data-aos-duration="600"
      data-aos-easing="linear"
      data-aos-delay="100"
      class="proficiency"
    >
      proficiency/stacks
    </h4>
    <div class="stacks">
      <h6
        data-aos="fade-up"
        data-aos-duration="600"
        data-aos-easing="linear"
        data-aos-delay="170"
      >
        Accessibility Conscious Web development standards Semantic HTML Version
        control (Git) Best practices
      </h6>
      <h6
        data-aos="fade-up"
        data-aos-duration="600"
        data-aos-easing="linear"
        data-aos-delay="220"
      >
        HTML, CSS, JS Vue / React, Next.JS TypeScript, CSS-in-JS CMS Build tools
        (Webpack, Babel, Vite)
      </h6>
      <h6
        data-aos="fade-up"
        data-aos-duration="600"
        data-aos-easing="linear"
        data-aos-delay="270"
      >
        CSS best practices Advanced SCSS/Sass Scalable and systemized style code
        BEM & other CSS methodologies ES6 Javascript
      </h6>
    </div>
    <Works />
    <h4
      data-aos="fade-up"
      data-aos-duration="500"
      data-aos-easing="linear"
      data-aos-delay="0"
    >
      experience
    </h4>
    <p
      class="exp"
      data-aos="fade-up"
      data-aos-duration="500"
      data-aos-easing="linear"
      data-aos-delay="100"
    >
      i’ve had experience working with a couple of amazing organizations/had
      hands-on experience on freelance projects as well.
    </p>
    <div class="experience">
      <div v-for="item in exp" :key="item.id">
        <h3>{{ item.company }}</h3>
        <h6>{{ item.role }}</h6>
        <p>{{ item.year }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import Works from "./Works.vue";
import { ref, onMounted } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";
onMounted(() => {
  AOS.init();
});
const exp = ref([
  {
    id: 1,
    company: "Luxtech Co",
    role: "Frontend Developer, Intern",
    year: "2021",
  },
  {
    id: 2,
    company: "AyaTrades",
    role: "Frontend Developer, Intern",
    year: "2022",
  },
  {
    id: 3,
    company: "Stunning Saas",
    role: "Frontend Developer",
    year: "2022",
  },
]);
</script>

<style lang="scss" scoped>
@import "./home.scss";
</style>
