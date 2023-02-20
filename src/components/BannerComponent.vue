<template>
   <div class="banner">
    <div class="banner__left">
      <div class="banner__heading">Сообщайте о проблемах <br /> и контролируйте ход их исправления!</div>
      <div class="banner__subtitle">Не большое описание буквально в несколько предложений, <br /> занимающие не более трех строк.</div>
      <div class="banner__button">
        <button-component :isWhite="true"><span>Сообщить о проблеме</span></button-component>
      </div>
    </div>
    <div class="banner__right">
      <error-control />
    </div>
   </div>
</template>

<script>
import ErrorControl from  '../assets/images/ErrorControl.vue'
import ButtonComponent from './ButtonComponent.vue'

export default {
  name: 'BannerComponent',
  components: { ErrorControl, ButtonComponent }
}
</script>

<style lang="less" scoped>
.banner {
  display: flex;
  justify-content: space-between;
  gap: 103px;
  background-color: var(--accents-primary);
  border-radius: 12px;
  
  &__left {
    padding: 32px 0px 24px 24px;
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
  }

  &__heading {
    font-weight: 400;
    font-size: 32px;
    line-height: 120%;
    letter-spacing: 0.02em;
    color: var(--easy-black);
  }

  &__subtitle{
    font-weight: 400;
    font-size: 16px;
    line-height: 140%;
    letter-spacing: 0.02em;
    color: var(--easy-black);
    opacity: 0.6;
  }

  &__button {
    margin-top: 24px;
  }
  &__button span {
    font-weight: 400;
    font-size: 14px;
    line-height: 19px;
    letter-spacing: 0.02em;
    color: #000000;
  }

  &__right {
    padding: 16px 80px 24px 0px;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    box-sizing: border-box;
  }
}
</style>