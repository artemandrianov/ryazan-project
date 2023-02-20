<template>
  <div class="statistic">
    <div 
      class="statistic__content"
      v-for="(statistic, index) in statistics"
        :key="index"
      >
      <div class="statistic__number">
        {{ statistic.number }}
      </div>
      <div class="statistic__text">
        {{ statistic.text }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StatisticComponent',
  setup() {
    const statistics = [
      {
        number: '24 643',
        text: 'Пользователей'
      },
      {
        number: '5 626',
        text: 'Опубликовано обращений'
      },
      {
        number: '3 028',
        text: 'Решено проблем'
      }
    ]

    return { statistics }
  }
}
</script>

<style lang="less" scoped>
.statistic {
  display: flex;
  justify-content: space-between;
  gap: 30px;
  background-color: var(--accents-primary);
  border-radius: 12px;

  &__content {
    margin: 56px 60px;
    display: flex;
    align-items: center;
    gap: 4px;
    flex-direction: column;
    box-sizing: border-box;
  }
  &__number {
    font-weight: 400;
    font-size: 40px;
    line-height: 120%;
    text-align: center;
    letter-spacing: 0.02em;
    color: var(--easy-black);
  }
  &__text {
    font-size: 16px;
    line-height: 140%;
    text-align: center;
    letter-spacing: 0.02em;
    color: var(--easy-black);
    opacity: 0.6;
  }
}
</style>