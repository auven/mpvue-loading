<template>
  <div class="line-spin-fade-loader vue-loaders" :style="{
    width: size,
    height: size,
    borderWidth: root_borderWidth
  }">
    <div :style="{
      width: bottom_width,
      height: size,
      backgroundColor: color,
      borderRadius: bottom_borderRadius,
      top: bottom_top
    }"></div>
    <div :style="{
      backgroundColor: color,
      width: bottomRight_width,
      height: size,
      borderRadius: bottomRight_borderRadius,
      top: bottomRight_top,
      left: bottomRight_left
    }"></div>
    <div :style="{
      width: right_width,
      height: size,
      borderRadius: right_borderRadius,
      left: right_left,
      backgroundColor: color
    }"></div>
    <div :style="{
      backgroundColor: color,
      width: topRight_width,
      height: size,
      borderRadius: topRight_borderRadius,
      top: topRight_top,
      left: topRight_left
    }"></div>
    <div :style="{
      backgroundColor: color,
      width: top_width,
      height: size,
      borderRadius: top_borderRadius,
      top: top_top
    }"></div>
    <div :style="{
      backgroundColor: color,
      width: topLeft_width,
      height: size,
      borderRadius: topLeft_borderRadius,
      top: topLeft_top,
      left: topLeft_left
    }"></div>
    <div :style="{
      backgroundColor: color,
      width: left_width,
      height: size,
      borderRadius: left_borderRadius,
      left: left_left
    }"></div>
    <div :style="{
      backgroundColor: color,
      width: bottomLeft_width,
      height: size,
      borderRadius: bottomLeft_borderRadius,
      top: bottomLeft_top,
      left: bottomLeft_left
    }"></div>
  </div>
</template>

<script>
const TO_CORNER_RATIO = 13.64 / 15
const TO_SIDE_RATIO = 20 / 15
const WIDTH_RATIO = 5 / 15
const BORDER_RATIO = 2 / 15

export default {
  name: 'LineSpinFadeLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    root_borderWidth() {
      return `calc(${this.size} * ${TO_SIDE_RATIO})`
    },
    top_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    top_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    top_top() {
      return `calc(${this.size} * ${TO_SIDE_RATIO} * -1)`
    },
    topRight_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    topRight_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    topRight_top() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    },
    topRight_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    right_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    right_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    right_left() {
      return `calc(${this.size} * ${TO_SIDE_RATIO})`
    },
    bottomRight_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    bottomRight_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    bottomRight_top() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    bottomRight_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    bottom_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    bottom_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    bottom_top() {
      return `calc(${this.size} * ${TO_SIDE_RATIO})`
    },
    bottomLeft_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    bottomLeft_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    bottomLeft_top() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    bottomLeft_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    },
    left_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    left_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    left_left() {
      return `calc(${this.size} * ${TO_SIDE_RATIO} * -1)`
    },
    topLeft_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    topLeft_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    },
    topLeft_top() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    },
    topLeft_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    }
  }
}
</script>

<style scoped>
.vue-loaders.line-spin-fade-loader {
  top: auto;
  left: auto;
  border: 20px solid transparent;
  width: 15px;
  height: 15px;
}

.vue-loaders.line-spin-fade-loader > div {
  margin: 0;
}

@-webkit-keyframes line-spin-fade-loader {
  50% {
    opacity: 0.3;
  }
  100% {
    opacity: 1;
  }
}

@keyframes line-spin-fade-loader {
  50% {
    opacity: 0.3;
  }
  100% {
    opacity: 1;
  }
}

.line-spin-fade-loader {
  position: relative;
  top: -10px;
  left: -4px;
}
.line-spin-fade-loader > div:nth-child(1) {
  top: 20px;
  left: 0;
  -webkit-animation: line-spin-fade-loader 1.2s -0.84s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.84s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(2) {
  top: 13.63636px;
  left: 13.63636px;
  -webkit-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  transform: rotate(-45deg);
  -webkit-animation: line-spin-fade-loader 1.2s -0.72s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.72s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(3) {
  top: 0;
  left: 20px;
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
  -webkit-animation: line-spin-fade-loader 1.2s -0.6s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.6s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(4) {
  top: -13.63636px;
  left: 13.63636px;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
  -webkit-animation: line-spin-fade-loader 1.2s -0.48s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.48s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(5) {
  top: -20px;
  left: 0;
  -webkit-animation: line-spin-fade-loader 1.2s -0.36s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.36s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(6) {
  top: -13.63636px;
  left: -13.63636px;
  -webkit-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  transform: rotate(-45deg);
  -webkit-animation: line-spin-fade-loader 1.2s -0.24s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.24s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(7) {
  top: 0;
  left: -20px;
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
  -webkit-animation: line-spin-fade-loader 1.2s -0.12s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s -0.12s infinite ease-in-out;
}
.line-spin-fade-loader > div:nth-child(8) {
  top: 13.63636px;
  left: -13.63636px;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
  -webkit-animation: line-spin-fade-loader 1.2s 0s infinite ease-in-out;
  animation: line-spin-fade-loader 1.2s 0s infinite ease-in-out;
}
.line-spin-fade-loader > div {
  background-color: #fff;
  width: 4px;
  height: 35px;
  border-radius: 2px;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  width: 5px;
  height: 15px;
}
</style>
