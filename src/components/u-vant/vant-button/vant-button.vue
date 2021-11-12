<template>
  <button class='vant-button--default' :class='getClass()' :style='getStyle()'>
    <!--  <button :class='getClass()' :style='getStyle()'>-->
    <slot></slot>
  </button>
</template>

<script lang='ts'>
import Vue from 'vue';

export type ButtonType =
  | 'default'
  | 'primary'
  | 'success'
  | 'warning'
  | 'danger';
export type ButtonSize = 'large' | 'normal' | 'small' | 'mini';
type styleType = {
  color?: string,
  border?: number,
  borderColor?: string,
  background?: string
}

export type ButtonIconPosition = 'left' | 'right';
export default Vue.extend({
  name: 'vantButton',
  props: {
    color: {
      type: String,
      default: '',
    },
    //ButtonType: 'default' | 'primary' | 'info' | 'warning' | 'danger';
    type: {
      type: String,
      default: 'primary',
    },
    //是否加阴影
    shadow: {
      type: Boolean,
      default: false,
    },
    // 宽度rpx或 %
    width: {
      type: String,
      default: '100%',
    },
    //高度rpx
    height: {
      type: String,
      default: '96rpx',
    },
    //字体大小rpx
    size: {
      type: Number,
      default: 32,
    },
    bold: {
      type: Boolean,
      default: false,
    },
    margin: {
      type: String,
      default: '0',
    },
    //形状 circle(圆角), square(默认方形)，rightAngle(平角)
    shape: {
      type: String,
      default: 'square',
    },
    plain: {
      type: Boolean,
      default: false,
    },
    //link样式，去掉边框，结合plain一起使用
    link: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    //禁用后背景是否为灰色 （非空心button生效）
    disabledGray: {
      type: Boolean,
      default: false,
    },
    loading: {
      type: Boolean,
      default: false,
    },
    formType: {
      type: String,
      default: '',
    },
    openType: {
      type: String,
      default: '',
    },
    index: {
      type: [Number, String],
      default: 0,
    },
    //是否需要阻止重复点击【默认200ms】
    preventClick: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    getStyle() {
      if (this.color) {
        const style: styleType = {
          color: this.plain ? this.color : 'white',
        };

        if (!this.plain) {
          // Use background instead of backgroundColor to make linear-gradient work
          style.background = this.color;
        }
        // hide border when color is linear-gradient
        if (this.color.includes('gradient')) {
          style.border = 0;
        } else {
          style.borderColor = this.color;
        }
        console.log(style);
        return style;
      }
    },
    getClass() {
      console.log(this.type);
      // return [
      //   this.type ? `vant-button--${this.type}` : 'vant-button--default',
      //   this.plain ? 'vant-button' + this.type + '-outline' : 'vant-button--' + (this.type || 'primary'),
      // ];
    },
    // getStyle() {
    //   if (this.color) {
    //     const style = {
    //       color: this.plain ? this.color : 'white',
    //     };
    //
    //     if (!this.plain) {
    //       // Use background instead of backgroundColor to make linear-gradient work
    //       style.background = this.color;
    //     }
    //
    //     // hide border when color is linear-gradient
    //     if (this.color.includes('gradient')) {
    //       style.border = 0;
    //     } else {
    //       style.borderColor = this.color;
    //     }
    //
    //     return style;
    //   }
    // }
    // const onClick = (event: MouseEvent) => {
    //   if (props.loading) {
    //     event.preventDefault();
    //   } else if (!props.disabled) {
    //     emit('click', event);
    //     route();
    //   }
    // };
  },
  mounted() {

  },
});
</script>

<style scoped lang='scss'>
@import "src/components/u-vant/vant-styles/css-variables";

:root {
  --van-button-mini-height: $button-mini-height;
  --van-button-mini-padding: $button-mini-padding;
  --van-button-mini-font-size: $button-mini-font-size;
  --van-button-small-height: $button-small-height;
  --van-button-small-padding: $button-small-padding;
  --van-button-small-font-size: $button-small-font-size;
  --van-button-normal-padding: $button-normal-padding;
  --van-button-normal-font-size: $button-normal-font-size;
  --van-button-large-height: $button-large-height;
  --van-button-default-height: $button-default-height;
  --van-button-default-line-height: $button-default-line-height;
  --van-button-default-font-size: $button-default-font-size;
  --van-button-default-color: $button-default-color;
  --van-button-default-background-color: $button-default-background-color;
  --van-button-default-border-color: $button-default-border-color;
  --van-button-primary-color: $button-primary-color;
  --van-button-primary-background-color: $button-primary-background-color;
  --van-button-primary-border-color: $button-primary-border-color;
  --van-button-success-color: $button-success-color;
  --van-button-success-background-color: $button-success-background-color;
  --van-button-success-border-color: $button-success-border-color;
  --van-button-danger-color: $button-danger-color;
  --van-button-danger-background-color: $button-danger-background-color;
  --van-button-danger-border-color: $button-danger-border-color;
  --van-button-warning-color: $button-warning-color;
  --van-button-warning-background-color: $button-warning-background-color;
  --van-button-warning-border-color: $button-warning-border-color;
  --van-button-border-width: $button-border-width;
  --van-button-border-radius: $button-border-radius;
  --van-button-round-border-radius: $button-round-border-radius;
  --van-button-plain-background-color: $button-plain-background-color;
  --van-button-disabled-opacity: $button-disabled-opacity;
  --van-button-icon-size: $button-icon-size;
  --van-button-loading-icon-size: $button-loading-icon-size;
}

.vant-button {
  position: relative;
  display: inline-block;
  box-sizing: border-box;
  height: var(--van-button-default-height);
  margin: 0;
  padding: 0;
  font-size: var(--van-button-default-font-size);
  line-height: var(--van-button-default-line-height);
  text-align: center;
  border-radius: var(--van-button-border-radius);
  cursor: pointer;
  transition: opacity var(--van-animation-duration-fast);
  -webkit-appearance: none;

  &::before {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100%;
    height: 100%;
    background: var(--van-black);
    border: inherit;
    border-color: var(--van-black);
    border-radius: inherit; /* inherit parent's border radius */
    transform: translate(-50%, -50%);
    opacity: 0;
    content: ' ';
  }

  &:active::before {
    opacity: 0.1;
  }

  &--loading,
  &--disabled {
    &::before {
      display: none;
    }
  }

  &--default {
    color: var(--van-button-default-color);
    background: var(--van-button-default-background-color);
    border: var(--van-button-border-width) solid var(--van-button-default-border-color);
  }

  &--primary {
    color: var(--van-button-primary-color);
    background: var(--van-button-primary-background-color);
    border: var(--van-button-border-width) solid var(--van-button-primary-border-color);
  }

  &--success {
    color: var(--van-button-success-color);
    background: var(--van-button-success-background-color);
    border: var(--van-button-border-width) solid var(--van-button-success-border-color);
  }

  &--danger {
    color: var(--van-button-danger-color);
    background: var(--van-button-danger-background-color);
    border: var(--van-button-border-width) solid var(--van-button-danger-border-color);
  }

  &--warning {
    color: var(--van-button-warning-color);
    background: var(--van-button-warning-background-color);
    border: var(--van-button-border-width) solid var(--van-button-warning-border-color);
  }

  &--plain {
    background: var(--van-button-plain-background-color);

    &.van-button--primary {
      color: var(--van-button-primary-background-color);
    }

    &.van-button--success {
      color: var(--van-button-success-background-color);
    }

    &.van-button--danger {
      color: var(--van-button-danger-background-color);
    }

    &.van-button--warning {
      color: var(--van-button-warning-background-color);
    }
  }

  &--large {
    width: 100%;
    height: var(--van-button-large-height);
  }

  &--normal {
    padding: var(--van-button-normal-padding);
    font-size: var(--van-button-normal-font-size);
  }

  &--small {
    height: var(--van-button-small-height);
    padding: var(--van-button-small-padding);
    font-size: var(--van-button-small-font-size);
  }

  &__loading {
    color: inherit;
    font-size: inherit;

    .van-loading__spinner {
      color: currentColor;
      width: var(--van-button-loading-icon-size);
      height: var(--van-button-loading-icon-size);
    }
  }

  &--mini {
    height: var(--van-button-mini-height);
    padding: var(--van-button-mini-padding);
    font-size: var(--van-button-mini-font-size);

    & + .van-button--mini {
      margin-left: var(--van-padding-base);
    }
  }

  &--block {
    display: block;
    width: 100%;
  }

  &--disabled {
    cursor: not-allowed;
    opacity: var(--van-button-disabled-opacity);
  }

  &--loading {
    cursor: default;
  }

  &--round {
    border-radius: var(--van-button-round-border-radius);
  }

  &--square {
    border-radius: 0;
  }

  // align-items are ignored when flex container is a button in legacy safari
  // see: https://bugs.webkit.org/show_bug.cgi?id=169700
  &__content {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;

    // fix icon vertical align
    // see: https://github.com/youzan/vant/issues/7617
    &::before {
      content: ' ';
    }
  }

  &__icon {
    font-size: var(--van-button-icon-size);
    line-height: inherit;
  }

  &__icon + &__text,
  &__loading + &__text,
  &__text + &__icon,
  &__text + &__loading {
    margin-left: var(--van-padding-base);
  }

  &--hairline {
    border-width: 0;

    &::after {
      border-color: inherit;
      border-radius: calc(var(--van-button-border-radius) * 2);
    }

    &.van-button--round::after {
      border-radius: var(--van-button-round-border-radius);
    }

    &.van-button--square::after {
      border-radius: 0;
    }
  }
}
</style>
