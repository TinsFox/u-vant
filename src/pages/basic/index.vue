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
        title: '基础组件',
        type: 'basic',
        items: [
          {path: 'button', title: 'Button 按钮'},
          {path: 'cell', title: 'Cell 单元格'},
          {path: 'config-provider', title: 'ConfigProvider 全局配置'},
          {path: 'typography', title: 'Typography 文本'},
          {path: 'icon', title: 'Icon 图标'},
          {path: 'image', title: 'Image 图片'},
          {path: 'popup', title: 'Popup 弹出层'},
          {path: 'styles', title: 'Style 内置样式'},
          {path: 'toast', title: 'Toast 轻提示'},
        ],
      }
    }
  },
  onLoad() {
  },
  methods: {}
})
</script>

