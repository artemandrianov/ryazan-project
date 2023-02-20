<template>
  <div class="info-component">
    <info-card
      v-for="(infoCard, i) in infoCards" 
      :key="i" 
      :infoCard="infoCard"
      class="info-component__content"
    />
    <tree-man-dog class="info-component__image"/>
  </div>
</template>

<script>
import InfoCard from './cards/InfoCard.vue'
import TreeManDog from '../assets/images/TreeManDog.vue'
import IconManagementBuild from '../assets/images/IconManagementBuild.vue'
import IconComplaint from '../assets/images/IconComplaint.vue'
import HelpSurveys from '../assets/images/HelpSurveys.vue'
import TooltypeDiscussion from '../assets/images/TooltypeDiscussion.vue'
import StarRating from '../assets/images/StarRating.vue'
import IconResponsible from '../assets/images/IconResponsible.vue'
import ManagementBuild from '../assets/images/ManagementBuild.vue'

export default {
  components: { InfoCard, TreeManDog },
  setup() {
    const infoCards = [
      {
        icon: IconManagementBuild, // link to icon
        contentImage: '', // link to house
        title: 'Мои управляющие организации',
        text: 'Не большое описание буквально в несколько строк.',
        showMore: 'xyu', // link
        imageBig: ManagementBuild
      },
      {
        icon: IconComplaint, // link to icon
        title: 'Жалобы и обращения',
        text: 'Тут проводятся опросы несколько строк не больше чем 3 строки.',
        showMore: 'xyu' // link
      }, 
      {
        icon: HelpSurveys, // link to icon
        title: 'Опросы',
        text: 'Не большое описание буквально в несколько предложений, занимающие не более трех строк.'
      },
      {
        icon: TooltypeDiscussion, // link to icon
        title: 'Общественные обсуждения',
        text: 'Не большое описание буквально в несколько предложений, занимающие не более трех строк.'
      },
      {
        icon: StarRating, // link to icon
        title: 'Рейтинги и исполнители',
        text: 'Не большое описание буквально в несколько предложений, занимающие не более трех строк.'
      },
      {
        icon: IconResponsible, // link to icon
        title: 'Уполномоченный по правам человека в Рязанской обл.',
        text: 'Не большое описание буквально в несколько предложений, занимающие не более трех строк.'
      }
    ]

    return { infoCards }
  }
}
</script>

<style lang="less" scoped>
.info-component {
  margin-top: 16px;
  box-sizing: border-box;
  display: grid;
  width: 100%;
  gap: 15px;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  
  &__content:first-child {
    grid-column: span 2;
    position: relative;
  }

  &__image {
    position: absolute;
    top: 1055px;
    left: 780px;
  }
}
</style>