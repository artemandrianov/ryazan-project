<template>
  <div class="info-card">
    <div class="info-card__content">
      <div class="info-card__icon">
        <component :is="infoCard.icon" />
      </div>
      <div class="info-card__title">
        {{ infoCard.title }}
      </div>
      <div class="info-card__text">
        {{ infoCard.text }}
      </div>
        <div 
          v-if="infoCard.showMore"
          :link="infoCard.showMore"
          class="info-card__button"
        >
          <button-component>Подробнее</button-component>
        </div>
    </div>
    <div class="info-card__image">
      <component 
        :is="infoCard.imageBig"
        class="info-card__component"
      />
    </div>
  </div>
</template>
<script>
import ButtonComponent from '../ButtonComponent.vue';

export default {
  name: 'InfoCard',
  components: { ButtonComponent },
  props: {
    infoCard: {
      type: Object,
      default: () => ({})
    }
  }
}
</script>
<style lang="less" scoped>
.info-card {
  padding: 24px 22px 24px 24px;
  background: #FFFFFF;
  border-radius: 12px;
  display: flex;
  justify-content: space-between;
  box-sizing: border-box;
  
  
  &__content {
    display: flex;
    flex-direction: column;
  }

  &__title {
    font-weight: 400;
    font-size: 24px;
    line-height: 120%;
    letter-spacing: 0.02em;
    color: #000000;
    margin-top: 29px;
  }

  &__text {
    font-weight: 400;
    font-size: 16px;
    line-height: 140%;
    letter-spacing: 0.02em;
    color: #000000;
    opacity: 0.6;
    margin-top: 29px;
    width: 250px;
  }

  &__button {
    margin-top: 24px;
  }

  &__image {
    position: absolute;
  }
    &__component {
      position: relative;
      margin: 42px 56px 0 354px;
    }
}
</style>