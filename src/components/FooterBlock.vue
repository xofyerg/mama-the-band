<template>
  <div class="footer">
    <div class="footer__content">
      ООО Группа М.А.М.А. - музыкальная организация. <br />
      Участники группы являются невымышленными персонажами. <br />

      Если вы хотите материально поддержать начинающих молодых музыкантов,
      направляйте донаты по ссылке ниже: <br />
      99% пожертвований уходит барабанщику.

      <div>
        <a class="footer__link" href="https://vk.com/xofyerg" target="_blank"
          >Поддержать группу
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  padding: 25px;
  background-color: #323232;
}

.footer__content {
  width: 460px;
  color: #ffffff;
  font-size: 12px;
  line-height: 18px;
}

.footer__link {
  display: inline-block;
  color: #cccccc;
  padding: 6px;
  border-radius: 4px;
  margin-top: 2px;
}
.footer__link:hover {
  background-color: rgba(0, 0, 0, 0.2);
  transition: 0.1s ease;
}

@media (max-width: 500px) {
  .footer__content {
    width: 100%;
  }
}
</style>
