<template>
  <div>
    <div class='title'>{{ title }}</div>
    <slot />
  </div>
</template>

<script>
export default {
  name: 'demo-block',
  props: {
    title: {
      type: String,
      default: 'u-vant',
    },
  },
};
</script>

<style scoped>
.title{
  margin: 0;
  padding: 32px 16px 16px;
  color: rgba(69, 90, 100, 0.6);
  font-weight: normal;
  font-size: 14px;
  line-height: 16px;
}
</style>
