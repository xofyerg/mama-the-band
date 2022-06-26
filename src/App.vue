<template>
  <hero-block :hero="hero" />
  <header-block />

  <my-swiper :synthImgs="synthImgs" />
</template>

<script>
import { info } from "@/helpers/data";
import HeroBlock from "@/components/HeroBlock";
import HeaderBlock from "@/components/HeaderBlock";
import MySwiper from "@/components/UI/MySwiper";
import "swiper/css";
import "swiper/css/effect-fade";
import "swiper/css/navigation";
import "swiper/css/pagination";

export default {
  components: {
    HeroBlock,
    HeaderBlock,
    MySwiper,
  },
  data() {
    return {
      hero: info.hero,
      synthImgs: [
        { value: "https://swiperjs.com/demos/images/nature-1.jpg", id: 1 },
        { value: "https://swiperjs.com/demos/images/nature-2.jpg", id: 2 },
        { value: "https://swiperjs.com/demos/images/nature-3.jpg", id: 3 },
        { value: "https://swiperjs.com/demos/images/nature-4.jpg", id: 4 },
      ],
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}

body {
  font-family: "Rubik", sans-serif;
  scroll-behavior: smooth;
}
</style>
