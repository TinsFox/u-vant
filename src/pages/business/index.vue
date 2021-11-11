<template>
  <div>
    <component-list :nav="nav"/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nav: {
        name: '业务组件',
        type: "business",
        items: [
          {path: 'area', title: 'Area 省市区选择'},
          {path: 'card', title: 'Card 卡片'},
          {path: 'coupon-list', title: 'Coupon 优惠券'},
          {path: 'submit-bar', title: 'SubmitBar 提交订单栏'},
          {path: 'sku', title: 'Sku 商品规格'},
        ],
      }
    }
  },
  onLoad() {

  },
  methods: {}
}
</script>

