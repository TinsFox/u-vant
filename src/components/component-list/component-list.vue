<template>
  <div>
    <div class="demo">
      <image class="logo" :src="logo"></image>
<!--      <text class="title">{{ nav.title }}</text>-->
      <navigator v-for="(item,index) in nav.items" :key="index" class="component-item"
                 :url="`/pages/${nav.type}/${item.path}`" hover-class="navigator-hover">
        <div>
          {{ item.title }}
        </div>
      </navigator>
      <!-- TODO 右侧图标-->
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

interface INav {
  title: string
  type: string
  items: Array<{ path: string, title: string }>
}

export default Vue.extend({
  name: "component-list",
  props: {
    nav: {
      type: Object,
      default: {}
    }
  },
  data() {
    return {
      logo: "https://img.yzcdn.cn/vant/logo.png"
    }
  }
})
</script>

<style scoped lang="scss">

.logo {
  height: 100rpx;
  width: 100rpx;
  margin: 40rpx auto 50rpx;
}

.demo {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0 auto 10px;
}

.title {
  text-align: left;
  color: $gray-4;
  align-self: flex-start;
}

.component-item {
  position: relative;
  display: flex;
  margin: 0 0 12px;
  padding-left: 20px;
  color: #323233;
  font-weight: 600;
  font-size: 14px;
  line-height: 40px;
  background: #f7f8fa;
  border-radius: 99px;
  transition: background .3s;
  width: 80%;
}
</style>
