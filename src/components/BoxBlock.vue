<template>
  <div class="box">
    <my-swiper :images="images" />

    <div class="box-text-right" v-if="isRight">
      <div class="box-text__content">
        <slot />
      </div>
    </div>
    <div class="box-text-left" v-else>
      <div class="box-text__content">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
import MySwiper from "@/components/UI/MySwiper";

export default {
  components: {
    MySwiper,
  },
  props: {
    images: {
      type: Array,
      required: true,
    },
    isRight: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
.box {
  height: 100vh;
  overflow: hidden;
  position: relative;
}

.box-text-left {
  position: absolute;
  left: 0;
  bottom: 0;
  top: 0;
  z-index: 1;
  max-width: 425px;
  width: 100%;
  background-color: #323232;
}

.box-text-left::before {
  content: "";
  position: absolute;
  right: -100px;
  border-bottom: 100vh solid #323232;
  border-right: 100px solid transparent;
}

.box-text-right {
  position: absolute;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 1;
  max-width: 425px;
  width: 100%;
  background-color: #323232;
}

.box-text-right::before {
  content: "";
  position: absolute;
  left: -100px;
  top: 0;
  border-bottom: 100vh solid #323232;
  border-left: 100px solid transparent;
}

.box-text__content {
  display: grid;
  place-items: center;
  height: 100%;
  padding: 25px 40px;
  font-size: 27px;
  box-sizing: border-box;
  color: #ffffff;
}
</style>
