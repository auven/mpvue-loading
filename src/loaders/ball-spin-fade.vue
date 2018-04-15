<template>
  <div class="ball-spin-fade-loader vue-loaders" :style="{
    width: size,
    height: size,
    borderWidth: root_borderWidth
  }">
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      top: bottom_top
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      top: bottomRight_top_left,
      left: bottomRight_top_left
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      left: right_left
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      top: topRight_top,
      left: topRight_left
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      top: top_top
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      top: topLeft_top_left,
      left: topLeft_top_left
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      left: left_left
    }"></div>
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color,
      top: bottomLeft_top,
      left: bottomLeft_left
    }"></div>
  </div>
</template>

<script>
const TO_CORNER_RATIO = 17.05 / 15
const TO_SIDE_RATIO = 25 / 15

export default {
  name: 'BallSpinFadeLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    root_borderWidth() {
      return `calc(${this.size} * ${TO_SIDE_RATIO})`
    },
    top_top() {
      return `calc(${this.size} * ${TO_SIDE_RATIO} * -1)`
    },
    topRight_top() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    },
    topRight_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    right_left() {
      return `calc(${this.size} * ${TO_SIDE_RATIO})`
    },
    bottomRight_top_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    bottom_top() {
      return `calc(${this.size} * ${TO_SIDE_RATIO})`
    },
    bottomLeft_top() {
      return `calc(${this.size} * ${TO_CORNER_RATIO})`
    },
    bottomLeft_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    },
    left_left() {
      return `calc(${this.size} * ${TO_SIDE_RATIO} * -1)`
    },
    topLeft_top_left() {
      return `calc(${this.size} * ${TO_CORNER_RATIO} * -1)`
    }
  }
}
</script>

<style scoped>
.vue-loaders.ball-spin-fade-loader {
  top: auto;
  left: auto;
  border: 25px solid transparent;
  width: 15px;
  height: 15px;
}

.vue-loaders.ball-spin-fade-loader > div {
  margin: 0;
}

@-webkit-keyframes ball-spin-fade-loader {
  50% {
    opacity: 0.3;
    -webkit-transform: scale(0.4);
    transform: scale(0.4);
  }
  100% {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@keyframes ball-spin-fade-loader {
  50% {
    opacity: 0.3;
    -webkit-transform: scale(0.4);
    transform: scale(0.4);
  }
  100% {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

.ball-spin-fade-loader {
  position: relative;
  top: -10px;
  left: -10px;
}
.ball-spin-fade-loader > div:nth-child(1) {
  top: 25px;
  left: 0;
  -webkit-animation: ball-spin-fade-loader 1s -0.96s infinite linear;
  animation: ball-spin-fade-loader 1s -0.96s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(2) {
  top: 17.04545px;
  left: 17.04545px;
  -webkit-animation: ball-spin-fade-loader 1s -0.84s infinite linear;
  animation: ball-spin-fade-loader 1s -0.84s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(3) {
  top: 0;
  left: 25px;
  -webkit-animation: ball-spin-fade-loader 1s -0.72s infinite linear;
  animation: ball-spin-fade-loader 1s -0.72s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(4) {
  top: -17.04545px;
  left: 17.04545px;
  -webkit-animation: ball-spin-fade-loader 1s -0.6s infinite linear;
  animation: ball-spin-fade-loader 1s -0.6s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(5) {
  top: -25px;
  left: 0;
  -webkit-animation: ball-spin-fade-loader 1s -0.48s infinite linear;
  animation: ball-spin-fade-loader 1s -0.48s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(6) {
  top: -17.04545px;
  left: -17.04545px;
  -webkit-animation: ball-spin-fade-loader 1s -0.36s infinite linear;
  animation: ball-spin-fade-loader 1s -0.36s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(7) {
  top: 0;
  left: -25px;
  -webkit-animation: ball-spin-fade-loader 1s -0.24s infinite linear;
  animation: ball-spin-fade-loader 1s -0.24s infinite linear;
}
.ball-spin-fade-loader > div:nth-child(8) {
  top: 17.04545px;
  left: -17.04545px;
  -webkit-animation: ball-spin-fade-loader 1s -0.12s infinite linear;
  animation: ball-spin-fade-loader 1s -0.12s infinite linear;
}
.ball-spin-fade-loader > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
}
</style>
