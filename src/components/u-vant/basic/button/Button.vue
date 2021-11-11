<template>
  <div>
    <button>按钮</button>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    //ButtonType: 'default' | 'primary' | 'info' | 'warning' | 'danger';
    type: {
      type: String,
      default: 'primary'
    },
    //是否加阴影
    shadow: {
      type: Boolean,
      default: false
    },
    // 宽度rpx或 %
    width: {
      type: String,
      default: '100%'
    },
    //高度rpx
    height: {
      type: String,
      default: '96rpx'
    },
    //字体大小rpx
    size: {
      type: Number,
      default: 32
    },
    bold: {
      type: Boolean,
      default: false
    },
    margin: {
      type: String,
      default: '0'
    },
    //形状 circle(圆角), square(默认方形)，rightAngle(平角)
    shape: {
      type: String,
      default: 'square'
    },
    plain: {
      type: Boolean,
      default: false
    },
    //link样式，去掉边框，结合plain一起使用
    link: {
      type: Boolean,
      default: false
    },
    disabled: {
      type: Boolean,
      default: false
    },
    //禁用后背景是否为灰色 （非空心button生效）
    disabledGray: {
      type: Boolean,
      default: false
    },
    loading: {
      type: Boolean,
      default: false
    },
    formType: {
      type: String,
      default: ''
    },
    openType: {
      type: String,
      default: ''
    },
    index: {
      type: [Number, String],
      default: 0
    },
    //是否需要阻止重复点击【默认200ms】
    preventClick: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>

</style>
