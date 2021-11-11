<template>
  <div class="demo">
    <!--    <div class="title">{{ list.name }}</div>-->
    <navigator v-for="(item,index) in list.items" :key="index" class="component-item"
               :url="`/pages/${list.type}/${item.path}`" hover-class="navigator-hover">
      <div>
        {{ item.title }}
      </div>
    </navigator>
    <!--    右侧图标-->
  </div>
</template>

<script>
export default {
  name: "component-list",
  props: {
    list: {
      type: Object,
      default: {}
    }
  }
}
</script>

<style scoped lang="scss">
.demo {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0 auto 10px;
}

.title {
  color: $gray-4;
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
