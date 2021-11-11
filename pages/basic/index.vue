<template>
  <div>
    <page-header title="基础组件"/>
    <component-list :list="list"/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: {
        name: '基础组件',
        type:'basic',
        items: [
          { path: 'button', title: 'Button 按钮' },
          { path: 'cell', title: 'Cell 单元格' },
          { path: 'config-provider', title: 'ConfigProvider 全局配置' },
          { path: 'typography', title: 'Typography 文本' },
          { path: 'icon', title: 'Icon 图标' },
          { path: 'image', title: 'Image 图片' },
          { path: 'popup', title: 'Popup 弹出层' },
          { path: 'styles', title: 'Style 内置样式' },
          { path: 'toast', title: 'Toast 轻提示' },
        ],
      }
    }
  },
  onLoad() {
    const str = "Button 按钮"
    const words = str.split(' ');
    console.log(words[0].toLowerCase())
    console.log(words[3]);
  },
  methods: {}
}
</script>

