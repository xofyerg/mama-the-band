<template>
  <hero-block :hero="hero" />
  <header-block />

  <box-block :images="synthImages"
    >Маша - наша клавишница. Знает ноты как свои пять пальцев, но не
    знает</box-block
  >
  <my-delimiter />
  <box-block :images="synthImages" :isRight="true"></box-block>
  <my-delimiter />
  <box-block :images="synthImages"></box-block>
  <my-delimiter />
  <box-block :images="synthImages" :isRight="true"></box-block>
  <my-delimiter />
  <box-block :images="synthImages"></box-block>
</template>

<script>
import { info } from "@/helpers/data";
import HeroBlock from "@/components/HeroBlock";
import HeaderBlock from "@/components/HeaderBlock";
import BoxBlock from "@/components/BoxBlock";
import MyDelimiter from "@/components/UI/MyDelimiter";
import "swiper/css";
import "swiper/css/effect-fade";
import "swiper/css/navigation";
import "swiper/css/pagination";

export default {
  components: {
    BoxBlock,
    HeroBlock,
    HeaderBlock,
    MyDelimiter,
  },
  data() {
    return {
      hero: info.hero,
      synthImages: [
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
