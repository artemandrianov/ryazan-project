<template>
  <header-block />
  <main-block />
  <footer-block />
</template>

<script>
import HeaderBlock from '../blocks/HeaderBlock.vue'
import MainBlock from '../blocks/MainBlock.vue'
import FooterBlock from '../blocks/FooterBlock.vue'

export default {
  name: 'ContentView',
  components: { HeaderBlock, MainBlock, FooterBlock }
}
</script>

<style lang="less" scoped>

</style>