<template>
  <div class="hero">
    <my-backdrop />

    <h1 class="hero__title">
      <div><slot></slot></div>
    </h1>
  </div>
</template>

<script>
import MyBackdrop from "@/components/UI/MyBackdrop";

export default {
  components: {
    MyBackdrop,
  },
};
</script>

<style scoped>
.hero {
  width: 100%;
  height: 100vh;
  position: relative;
  display: grid;
  place-items: center;
  overflow: hidden;
  background: url("../assets/hero.jpg");
  background-size: cover;
}

.hero__title {
  position: absolute;
  color: #fff;
  font-size: 48px;
  text-align: center;
}
</style>
