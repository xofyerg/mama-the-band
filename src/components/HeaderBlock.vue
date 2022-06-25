<template>
  <header class="header">
    <ul>
      <li><a href="#">Мария</a></li>
      <li><a href="#">Александр</a></li>
      <li><a href="#">Михаил</a></li>
      <li><a href="#">Александр</a></li>
    </ul>
  </header>
</template>

<script>
export default {
  name: "HeaderBlock",
};
</script>

<style scoped>
.header {
  max-width: 100%;
  display: flex;
  display: -ms-flex;
  display: -webkit-flex;
  font-size: 17px;
  background: -webkit-linear-gradient(45deg, #040d2c, #462a8b, #c505d6);
  background: linear-gradient(45deg, #040d2c, #462a8b, #c505d6);
}

ul {
  margin: 14px auto;
  display: flex;
  display: -ms-flex;
  display: -webkit-flex;
  gap: 60px;
}

a {
  color: #fff;
}
</style>
