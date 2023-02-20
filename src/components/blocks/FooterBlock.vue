<template>
  <footer class="footer-block">
    <div class="footer-block__container">
      <div class="footer-block__primary">
        <footer-logo />
        <div class="footer-block__text">Информационная экосистема Рязанской области — <br />Наш Дом Рязань</div>
      </div>
      <div class="footer-block__navigation"></div>
    </div>
    <div class="footer-block__technical">
      <div class="footer-block__copyright"></div>
      <div class="footer-block__store"></div>
    </div>
  </footer>
</template>

<script>
import FooterLogo from '../../assets/images/FooterLogo.vue'

export default {
  name: 'FooterBlock',
  components: { FooterLogo }
}
</script>

<style lang="less" scoped>
.footer-block {
  padding: 0 195px;
  background-color: #FFFFFF;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__container {
    margin-top: 48px;
    margin-bottom: 72px;
  }
  &__text {
    font-weight: 400;
    font-size: 14px;
    line-height: 140%;
    letter-spacing: 0.02em;
    color: #1B1400;
    width: 150px;
  }
}
</style>