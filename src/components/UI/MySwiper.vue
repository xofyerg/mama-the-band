<template>
  <swiper
    :spaceBetween="30"
    :effect="'fade'"
    :loop="true"
    :autoplay="{
      delay: 2000,
      disableOnInteraction: false,
    }"
    :modules="modules"
    class="my-swiper"
  >
    <swiper-slide v-for="image in images" :key="image.id">
      <img :src="image.value" alt="" />
    </swiper-slide>
  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { EffectFade, Autoplay } from "swiper";

export default {
  name: "my-swiper",
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  setup() {
    return {
      modules: [EffectFade, Autoplay],
    };
  },
};
</script>

<style scoped>
.my-swiper {
  position: absolute;
  width: 100%;
  height: 100%;
  right: 0;
}

.my-swiper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
