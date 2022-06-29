<template>
  <header class="header">
    <ul>
      <li><a href="#synth">Мария</a></li>
      <li><a href="#guitar">Александр</a></li>
      <li><a href="#drums">Михаил</a></li>
      <li><a href="#bass">Александр</a></li>
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
  background-color: rgba(32, 32, 32, 0.8);
  display: grid;
  place-items: center;
  height: 3em;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 10;
}

ul {
  display: flex;
}

a {
  padding: 9px 36px;
  color: #ffffff;
  border-radius: 6px;
  font-size: 14px;
}
a:hover {
  background-color: rgba(0, 0, 0, 0.2);
  transition: 0.1s ease;
}

@media (max-width: 540px) {
  .header {
    display: none;
  }
}
</style>
