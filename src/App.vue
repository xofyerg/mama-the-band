<template>
  <div class="app">
    <hero-block>
      <div>
        Привет! Это М.А.М.А. <br />
        Мы группа молодых энтузиастов
      </div>
    </hero-block>
    <header-block />

    <box-block :images="info.synth" id="synth">
      <h1>Мария М.</h1>
      <p>
        Клавишница со стажем. Может сыграть Франца Фердинанта с закрытыми
        глазами.
      </p>
      <p>
        Очень холодна и расчетлива, из-за чего участники группы думают, что она
        киборг-убийца, присланный из будущего. Хорошо владеет английским языком,
        даже лучше, чем русским.
      </p>
      <p>
        Мария может с легкостью вкатится в любую компанию, как нож в масло,
        поэтому рекомендуется использовать ее, если вам не достает еще парочки
        человек для вашей невероятной вечеринки, либо же, если вам нужна ширма
        для ванны.
      </p>
    </box-block>

    <box-block :images="info.guitar" :isRight="true" id="guitar">
      <h1>Александр П.</h1>
      <p>
        Гитарист, басист, барабанщик, клавишник, вокалист, солист, баскетболист,
        волейболист, футболист, нигилист, фаталист, монополист и многое-многое
        другое.
      </p>
      <p>
        К сожалению, данного текстового блока не хватит, чтобы рассказать о всех
        заслугах Александра, поэтому ограничимся лишь двумя процентами от общего
        количества.
      </p>
      <p>
        Увлекается музыкой с 0 лет и способен заменить любого участника этой
        группы, находится здесь только потому, что ему не с кем выпить пива.
      </p>
    </box-block>
    <box-block :images="info.drums" id="drums">
      <h1>Михаил М.</h1>
      <p>
        Начинающий барабанщик. До сих пор не понимает, как открыл для себя мир
        барабанов и вообще в целом ничего не понимает.
      </p>
      <p>
        Любит пиццу с ананасами, в связи с этим является изгоем общества и
        порицается всеми участниками группы.
      </p>
      <p>
        Неисправимый оптимист, недопонятый гений, какой-то мужик и еще пару
        красивых слов.
      </p>
    </box-block>
    <box-block :images="info.bass" :isRight="true" id="bass">
      <h1>Александр К.</h1>
      <p>
        Непревзойденный басист. Может играть только в перчатках из-за того, что
        любые наэлектризованные предметы бьют его током.
      </p>
      <p>
        Долгое время пытался бросить курить, что и привело его в группу. Толстые
        струны баса оказались лучшим лекарством.
      </p>
      <p>
        Продал айфон, чтобы купить всем участникам группы инструменты, но в
        итоге хватило только на барабаны.
      </p>
      <p>
        В свое время сыграл эпизодическую роль шпаги Кота в сапогах в
        мультфильме "Шрек".
      </p>
    </box-block>
    <box-block :images="info.mot">
      <h1>Мот</h1>
      <p>Наш пиар-менеджер и талисман группы.</p>
      <p>
        Любит плотно погулять и вкусно покушать. Без Мота не было бы и всей
        группы.
      </p>
      <p>
        Буквально притягивает людей в своем окружении, так как обладает мощной
        харизмой и уверенностью в себе.
      </p>
    </box-block>

    <footer-block />

    <a href="#hero">
      <div class="app__btn" />
    </a>
  </div>
</template>

<script>
import { info } from "@/data";
import HeroBlock from "@/components/HeroBlock";
import HeaderBlock from "@/components/HeaderBlock";
import BoxBlock from "@/components/BoxBlock";
import FooterBlock from "@/components/FooterBlock";
import "swiper/css";
import "swiper/css/effect-fade";
import "swiper/css/navigation";
import "swiper/css/pagination";

export default {
  components: {
    BoxBlock,
    HeroBlock,
    HeaderBlock,
    FooterBlock,
  },
  data() {
    return {
      info,
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

html,
body {
  font-family: "Rubik", sans-serif;
  scroll-behavior: smooth;
}

::-webkit-scrollbar {
  width: 8px;
  background-color: #f9f9fd;
}
::-webkit-scrollbar-thumb {
  background-color: #323232;
}
::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.2);
  background-color: #f9f9fd;
}

a {
  text-decoration: none;
  display: block;
}

ul {
  list-style: none;
}

h1 {
  font-size: 38px;
  margin-bottom: 25px;
}

p {
  margin-bottom: 10px;
}

.app {
  position: relative;
}

.app__btn {
  width: 50px;
  height: 50px;
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-image: url("assets/up-arrow.png");
  background-repeat: no-repeat;
  opacity: 0.8;
  background-size: 50px;
  z-index: 10;
  cursor: pointer;
}
.app__btn:hover {
  opacity: 1;
  transition: 0.1s ease;
}

@media (max-width: 832px) {
  h1 {
    font-size: 20px;
  }
}
</style>
