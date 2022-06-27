<template>
  <hero-block>Привет! Это М.А.М.А. </hero-block>
  <header-block />

  <box-block :images="synth">
    <h1>Мария М.</h1>
    <p>
      Клавишница со стажем. Может сыграть Франца Фердинанта с закрытыми глазами.
    </p>
    <p>
      Очень холодна и расчетлива, из-за чего участники группы думают, что она
      киборг-убийца, которого прислали из будущего. Хорошо владеет английским
      языком, даже лучше, чем русским.
    </p>
    <p>
      Мария может с легкостью вкатится в любую компанию, как нож в масло,
      поэтому рекомендуется использовать ее, если вам не достает еще парочки
      человек для вашей невероятной вечеринки, либо же, если вам нужна ширма для
      ванны.
    </p>
  </box-block>
  <my-delimiter />
  <box-block :images="guitar" :isRight="true"
    ><h1>Александр П.</h1>
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
  <my-delimiter />
  <box-block :images="drums">
    <h1>Михаил М.</h1>
    <p>
      Начинающий барабанщик. До сих пор не понимает, как открыл для себя мир
      барабанов и вообще в целом ничего не понимает.
    </p>
    <p>
      Любит пиццу с ананасами, в связи с этим является изгоем общества и
      порицается всеми участниками группы.
    </p>
    <p></p>
  </box-block>
  <my-delimiter />
  <box-block :images="bass" :isRight="true">
    <h1>Александр К.</h1>
    <p>
      Непревзойденный басист. Может играть только в перчатках из-за того, что
      любые наэлектризованные предметы бьют его током.
    </p>
    <p>
      Продал айфон, чтобы купить всем участникам группы инструменты, в итоге
      хватило только на барабаны.
    </p>
  </box-block>
  <my-delimiter />
  <box-block></box-block>
</template>

<script>
import { info } from "@/helpers/data";
import HeroBlock from "@/components/HeroBlock";
import HeaderBlock from "@/components/HeaderBlock";
import BoxBlock from "@/components/BoxBlock";
import MyDelimiter from "@/components/UI/MyDelimiter";
import "swiper/css";
import "swiper/css/effect-fade";
import "swiper/css/navigation";
import "swiper/css/pagination";

export default {
  components: {
    BoxBlock,
    HeroBlock,
    HeaderBlock,
    MyDelimiter,
  },
  data() {
    return {
      hero: info.hero,
      synth: info.synth,
      guitar: info.guitar,
      drums: info.drums,
      bass: info.bass,
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}

body {
  font-family: "Rubik", sans-serif;
  scroll-behavior: smooth;
}

h1 {
  font-size: 38px;
  margin-bottom: 25px;
}

p {
  margin-bottom: 10px;
}
</style>
