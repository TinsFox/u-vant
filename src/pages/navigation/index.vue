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
        title: "导航组件",
        items: [
          {path: 'action-bar', title: 'ActionBar 动作栏'},
          {path: 'grid', title: 'Grid 宫格'},
          {path: 'index-bar', title: 'IndexBar 索引栏'},
          {path: 'nav-bar', title: 'NavBar 导航栏'},
          {path: 'pagination', title: 'Pagination 分页'},
          {path: 'sidebar', title: 'Sidebar 侧边导航'},
          {path: 'tabs', title: 'Tabs 标签页'},
          {path: 'tabbar', title: 'Tabbar 标签栏'},
        ],
      }
    }
  },
  onLoad() {

  },
  methods: {}
})
</script>

