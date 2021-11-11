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
        title: "表单组件",
        items: [
          {path: 'calendar', title: 'Calendar 日历'},
          {path: 'cascader', title: 'Cascader 级联选择'},
          {path: 'checkbox', title: 'Checkbox 复选框'},
          {path: 'datetime-picker', title: 'DatetimePicker 时间选择'},
          {path: 'field', title: 'Field 输入框'},
          {path: 'form', title: 'Form 表单'},
          {path: 'number-keyboard', title: 'NumberKeyboard 数字键盘'},
          {path: 'password-input', title: 'PasswordInput 密码输入框'},
          {path: 'picker', title: 'Picker 选择器'},
          {path: 'radio', title: 'Radio 单选框'},
          {path: 'rate', title: 'Rate 评分'},
          {path: 'search', title: 'Search 搜索'},
          {path: 'slider', title: 'Slider 滑块'},
          {path: 'stepper', title: 'Stepper 步进器'},
          {path: 'switch', title: 'Switch 开关'},
          {path: 'uploader', title: 'Uploader 文件上传'},
        ],
      }
    }
  },
  onLoad() {

  },
  methods: {}
})
</script>

