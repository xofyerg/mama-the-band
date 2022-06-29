<template>
  <div class="box">
    <my-swiper :images="images" />

    <div class="box-text-right" v-if="isRight">
      <div class="box-text__content">
        <div>
          <slot />
        </div>
      </div>
    </div>
    <div class="box-text-left" v-else>
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
  data() {
    return {
      isInit: true,
    };
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
  mounted() {
    this.isInit = false;
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
  width: 425px;
  background-color: rgba(32, 32, 32, 0.9);
}

.box-text-left::before {
  content: "";
  position: absolute;
  right: -100px;
  border-bottom: 100vh solid rgba(32, 32, 32, 0.9);
  border-right: 100px solid transparent;
}

.box-text-right {
  position: absolute;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 1;
  width: 425px;
  background-color: rgba(32, 32, 32, 0.9);
}

.box-text-right::before {
  content: "";
  position: absolute;
  left: -100px;
  top: 0;
  border-bottom: 100vh solid rgba(32, 32, 32, 0.9);
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

@media (max-width: 1024px) {
  .box-text__content {
    font-size: 16px;
    padding: 20px;
  }

  .box-text-left,
  .box-text-right {
    width: 300px;
  }
}

@media (max-width: 772px) {
  .box-text-left,
  .box-text-right {
    width: 100%;
  }
}

@media (max-height: 800px) {
  .box-text__content {
    font-size: 16px;
    padding: 20px;
  }
}
</style>
