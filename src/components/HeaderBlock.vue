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
  background-color: #323232;
  display: grid;
  place-items: center;
  height: 3em;
  box-shadow: 0 4px 4px rgba(0, 0, 0, 0.24);
}

ul {
  display: flex;
  gap: 60px;
}

a {
  display: block;
  padding: 9px;
  color: #ffffff;
}
</style>
