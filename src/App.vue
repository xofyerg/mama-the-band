<template>
  <hero-block :hero="hero" />
  <header-block />
</template>

<script>
import { info } from "@/helpers/data";
import HeroBlock from "@/components/HeroBlock";
import HeaderBlock from "@/components/HeaderBlock";

export default {
  components: {
    HeroBlock,
    HeaderBlock,
  },

  data() {
    return {
      hero: info.hero,
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
  color: #000;
}

ul {
  list-style: none;
}

body {
  font-family: "Rubik", sans-serif;
}
</style>
