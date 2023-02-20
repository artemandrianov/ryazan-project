<template>
  <div class="button" :class="{
    'button_white': isWhite
  }">
  <slot />
  </div>
</template>

<script>
export default {
  name: 'ButtonComponent',
  props: {
    isWhite: { type: Boolean, default: false }
  }
}
</script>

<style lang="less" scoped>
.button {
  cursor: pointer;
  width: max-content;
  padding: 8px 12px;
  border-radius: 8px;
  font-size: 14px;
  line-height: 18.59px;
  color: #FAFAFA;
  background-color: var(--accents-primary);
  
  &:hover {
    background: linear-gradient(0deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.2)), var(--accents-primary-hover);
  }
  &_small {
    padding: 8px 16px;
  }
      
  
  &_white {
    background-color: #fff;
    color: var(--easy-black);
  
    &:hover {
      color: #fff;
    }
  } 
}
</style>