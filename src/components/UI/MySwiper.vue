<template>
  <swiper
    :spaceBetween="30"
    :effect="'fade'"
    :modules="modules"
    class="my-swiper"
  >
    <swiper-slide v-for="synth in synthImgs" :key="synth.id">
      <img :src="synth.value" alt="" />
    </swiper-slide>
  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { EffectFade } from "swiper";

export default {
  name: "my-swiper",
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    synthImgs: {
      type: Array,
      required: true,
    },
  },
  setup() {
    return {
      modules: [EffectFade],
    };
  },
};
</script>

<style scoped>
.my-swiper {
  height: 100vh;
  overflow: hidden;
}

.my-swiper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
