<template>
  <header class="header-block">
    <div class="header-block__logo">
      <ryazan-logo />
    </div>
    <div class="header-block__navigation">
      <div>О проекте</div>
      <div>Помощь</div>
      <button-component class="header-block__button">
        <gov-services />
        <span>Войти</span>
      </button-component>
    </div>
  </header>
</template>

<script>
import RyazanLogo from '../../assets/images/RyazanLogo.vue'
import ButtonComponent from '../ButtonComponent.vue'
import GovServices from '../../assets/images/GovServices.vue';

export default {
  name: 'HeaderBlock',
  components: { RyazanLogo, ButtonComponent, GovServices }
}
</script>

<style lang="less" scoped>
.header-block {
  padding: 0 195px;
  background-color: #FFFFFF;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__logo {
    margin: 18px

  }

  &__navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 32px;
    font-weight: 400;
    font-size: 14px;
    line-height: 19px;
    letter-spacing: 0.02em;
    color: #1B1400;
  }

  &__button {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 9px;
    font-size: 14px;
    line-height: 19px;
    letter-spacing: 0.02em;
    color: #1B1400;
  }
}
</style>