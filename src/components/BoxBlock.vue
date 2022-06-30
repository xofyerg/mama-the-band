<template>
  <div class="box">
    <my-swiper :images="images" />

    <div class="box-text box-text__right" v-if="isRight">
      <div class="box-text__content">
        <div>
          <slot />
        </div>
      </div>
    </div>
    <div class="box-text box-text__left" v-else>
      <div class="box-text__content">
        <div>
          <slot />
        </div>
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

.box-text {
  position: absolute;
  bottom: 0;
  top: 0;
  z-index: 1;
  width: 29%;
  background-color: rgba(32, 32, 32, 0.9);
}
.box-text.box-text__left {
  left: 0;
}
.box-text.box-text__right {
  right: 0;
}

.box-text__left::before,
.box-text__right::before {
  content: "";
  position: absolute;
  border-bottom: 100vh solid rgba(32, 32, 32, 0.9);
}
.box-text__left::before {
  right: -100px;
  border-right: 100px solid transparent;
}
.box-text__right::before {
  left: -100px;
  border-left: 100px solid transparent;
}

.box-text__content {
  display: grid;
  place-items: center;
  height: 100%;
  padding: 15px 65px 15px 50px;
  font-size: 24px;
  box-sizing: border-box;
  color: #ffffff;
}

@media (max-width: 1440px) {
  .box-text__content {
    padding: 20px;
    font-size: 16px;
  }
}
@media (max-height: 832px) {
  .box-text__content {
    font-size: 16px;
  }
}

@media (max-width: 832px) {
  .box-text__content {
    font-size: 12px;
  }
}

@media (max-width: 572px) {
  .box-text {
    width: 100%;
    background-color: rgba(32, 32, 32, 0.8);
  }
  .box-text__content {
    font-size: 20px;
  }
}
</style>
