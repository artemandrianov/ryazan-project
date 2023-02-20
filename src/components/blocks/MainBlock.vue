<template>
  <div class="main-block">
    <banner-component class="main-block__banner" />
    <info-component class="main-block__info" />
    <statistic-component class="main-block__statistic" />
  </div>
</template>

<script>
import BannerComponent from '../BannerComponent.vue'
import InfoComponent from '../InfoComponent.vue'
import StatisticComponent from '../StatisticComponent.vue'

export default {
  name: 'MainBlock',
  components: { BannerComponent, InfoComponent, StatisticComponent }
}
</script>

<style lang="less" scoped>
.main-block {
  margin: 40px 195px;

  &__statistic {
    margin-top: 64px;
  }
}
</style>