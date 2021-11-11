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
        name: '反馈组件',
        type: 'action',
        items: [
          { path: 'action-sheet', title: 'ActionSheet 动作面板' },
          { path: 'dialog', title: 'Dialog 弹出框' },
          { path: 'dropdown-menu', title: 'DropdownMenu 下拉菜单' },
          { path: 'loading', title: 'Loading 加载' },
          { path: 'notify', title: 'Notify 消息通知' },
          { path: 'overlay', title: 'Overlay 遮罩层' },
          { path: 'pull-refresh', title: 'PullRefresh 下拉刷新' },
          { path: 'share-sheet', title: 'ShareSheet 分享面板' },
          { path: 'swipe-cell', title: 'SwipeCell 滑动单元格' },
        ],
      }
    }
  },
  onLoad() {

  },
  methods: {}
})
</script>

