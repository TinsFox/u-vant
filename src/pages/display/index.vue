<template>
  <div>
    <component-list :nav="nav"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  data() {
    return {
      nav: {
        name: '展示组件',
        items: [
          {path: 'badge', title: 'Badge 徽标'},
          {path: 'circle', title: 'Circle 环形进度条'},
          {path: 'collapse', title: 'Collapse 折叠面板'},
          {path: 'count-down', title: 'CountDown 倒计时'},
          {path: 'divider', title: 'Divider 分割线'},
          {path: 'image-preview', title: 'ImagePreview 图片预览'},
          {path: 'lazyload', title: 'Lazyload 懒加载'},
          {path: 'list', title: 'List 列表'},
          {path: 'skeleton', title: 'Skeleton 骨架屏'},
          {path: 'steps', title: 'Steps 步骤条'},
          {path: 'notice-bar', title: 'NoticeBar 通知栏'},
          {path: 'popover', title: 'Popover 气泡弹出框'},
          {path: 'progress', title: 'Progress 进度条'},
          {path: 'sticky', title: 'Sticky 粘性布局'},
          {path: 'swiper', title: 'Swiper 轮播'},
          {path: 'tag', title: 'Tag 标签'},
        ],
      }
    }
  },
  onLoad() {

  },
  methods: {}
})
</script>
