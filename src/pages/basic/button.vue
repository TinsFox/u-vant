<template>
  <div>
    <demo-block title='基础用法'>
      <vant-button type='primary'>主要按钮</vant-button>
      <vant-button type='info'>信息按钮</vant-button>
      <vant-button type='default'>默认按钮</vant-button>
      <vant-button type='warning'>警告按钮</vant-button>
      <vant-button type='danger'>危险按钮</vant-button>
      <div class='test'>测试</div>
    </demo-block>

  </div>
</template>

<script lang='ts'>


import Vue from 'vue';

export default Vue.extend({
  name: 'button-demo',
});
</script>

<style scoped lang='scss'>
@import "src/components/u-vant/vant-styles/css-variables";

.test {
color: var(--rv-red);
}
</style>
