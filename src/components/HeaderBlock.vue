<template>
  <header class="header">
    <div class="header__links">
      <ul>
        <li><a href="#synth">Мария</a></li>
        <li><a href="#guitar">Александр</a></li>
        <li><a href="#drums">Михаил</a></li>
        <li><a href="#bass">Александр</a></li>
      </ul>
    </div>

    <div class="header__links-hidden">
      <ul>
        <li><a href="#synth">М</a></li>
        <li><a href="#guitar">А</a></li>
        <li><a href="#drums">М</a></li>
        <li><a href="#bass">А</a></li>
      </ul>
    </div>
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

.header__links {
  display: inline;
}
.header__links-hidden {
  display: none;
}

@media (max-width: 540px) {
  .header__links {
    display: none;
  }
  .header__links-hidden {
    display: inline;
  }
  a {
    padding: 9px 26px;
  }
}
</style>
