<template>
  <content-view />
</template>

<script>
import ContentView from './components/views/ContentView.vue'

export default {
  name: 'App',
  components: { ContentView }
}
</script>

<style lang="less">
@import './assets/color.less';
body {
  background: #EFEFEF;
}

a,
a:visited {
  text-decoration: none;
  color: inherit;
}
</style>
