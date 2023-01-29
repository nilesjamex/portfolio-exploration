<template>
  <section class="home__work" id="works">
    <h4>selected works.</h4>
    <div class="home__work__content">
      <div class="items" v-for="item in works" :key="item.id">
        <a :href="item.link" target="__blank">
          <span>
            <img :src="item.img" alt="" width="240" height="240" />
          </span>
          <p>{{ item.name }} <img src="@/assets/arrow.svg" alt="" /></p>
        </a>
      </div>
    </div>
    <a href="http://github.com/nilesjamex" target="__blank" class="button">
      <button>SEE MORE OF MY PROJECTS ON GITHUB</button>
    </a>
  </section>
</template>

<script setup>
import { ref } from "vue";
const works = ref([
  {
    id: 1,
    img: "https://res.cloudinary.com/dx9pt4ggx/image/upload/v1674909500/portfolio/noxica_n7lnvz.png",
    name: "Noxica",
    link: "https://noxica.vercel.app/",
  },
  {
    id: 2,
    img: "https://res.cloudinary.com/dx9pt4ggx/image/upload/v1673194282/meta_rhyed6.png",
    name: "Panthone",
    link: "https://panthone.vercel.app/",
  },
  {
    id: 3,
    img: "https://res.cloudinary.com/dx9pt4ggx/image/upload/v1674909373/portfolio/floki_ze0awn.png",
    name: "WTF Foki",
    link: "https://www.wtffloki.com/",
  },
  {
    id: 4,
    img: "https://res.cloudinary.com/dx9pt4ggx/image/upload/v1672305605/Lendsqr/lendsqr-logo_pn2jeq.png",
    name: "lendsqr",
    link: "https://egbaidomehjames-lendsqr-fe-test.vercel.app/",
  },
  {
    id: 5,
    img: "https://res.cloudinary.com/dx9pt4ggx/image/upload/v1674909527/portfolio/panthone_wmf1h9.png",
    name: "Jemima",
    link: "https://jemima.vercel.app/",
  },
  {
    id: 6,
    img: "https://res.cloudinary.com/dx9pt4ggx/image/upload/v1674910800/portfolio/zerotech_y9emcn.png",
    name: "Zero to Tech",
    link: "https://dashboardzero.vercel.app/",
  },
]);
</script>

<style lang="scss" scoped>
@import "./home.scss";
</style>
