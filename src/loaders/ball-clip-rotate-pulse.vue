<template>
  <div class="ball-clip-rotate-pulse vue-loaders" :style="{
      width: rootStylesSize,
      marginLeft: rootStylesSize,
      height: stylesSize
    }">
    <div :style="{
      backgroundColor: color,
      width: innerBallStylesWidthHeight,
      height: innerBallStylesWidthHeight,
      top: innerBallStylesTop,
      left: innerBallStylesLeft
    }"></div>
    <div :style="{
      width: size,
      height: size,
      borderTopColor: color,
      borderBottomColor: color,
      top: outerBallStylesTop,
      left: outerBallStylesLeft,
      borderWidth: outerBallStylesBorderWidth
    }"></div>
  </div>
</template>

<script>
const BASE_SIZE_PX = '30px'
const BORDER_RATION = 2 / 30
const INNER_BALL_SIZE_RATION = 16 / 30
const INNER_BALL_OFFSET_RATION = 7 / 30

export default {
  name: 'BallClipRotatePulseLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    stylesSize() {
      return this.size ? String(this.size) : BASE_SIZE_PX
    },
    rootStylesSize() {
      return `calc(${this.stylesSize} / 2)`
    },
    outerBallStylesTop() {
      return `calc(${this.size} * -1 * ${BORDER_RATION})`
    },
    outerBallStylesBorderWidth() {
      return `calc(${this.size} * ${BORDER_RATION})`
    },
    outerBallStylesLeft() {
      return `calc(${this.size} * -1 * ${INNER_BALL_SIZE_RATION})`
    },
    innerBallStylesWidthHeight() {
      return `calc(${this.size} * ${INNER_BALL_SIZE_RATION})`
    },
    innerBallStylesTop() {
      return `calc(${this.size} * ${INNER_BALL_OFFSET_RATION})`
    },
    innerBallStylesLeft() {
      return `calc(${this.size} * -1 * ${INNER_BALL_OFFSET_RATION})`
    }
  }
}
</script>

<style scoped>
.vue-loaders.ball-clip-rotate-pulse {
  transform: none;
}
@keyframes rotate {
  0% {
    -webkit-transform: rotate(0deg) scale(1);
    transform: rotate(0deg) scale(1);
  }
  50% {
    -webkit-transform: rotate(180deg) scale(0.6);
    transform: rotate(180deg) scale(0.6);
  }
  100% {
    -webkit-transform: rotate(360deg) scale(1);
    transform: rotate(360deg) scale(1);
  }
}

@keyframes scale {
  30% {
    -webkit-transform: scale(0.3);
    transform: scale(0.3);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

.ball-clip-rotate-pulse {
  position: relative;
  -webkit-transform: translateY(-15px);
  -ms-transform: translateY(-15px);
  transform: translateY(-15px);
}
.ball-clip-rotate-pulse > div {
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  top: 0px;
  left: 0px;
  border-radius: 100%;
}
.ball-clip-rotate-pulse > div:first-child {
  background: #fff;
  height: 16px;
  width: 16px;
  top: 7px;
  left: -7px;
  -webkit-animation: scale 1s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
  animation: scale 1s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
}
.ball-clip-rotate-pulse > div:last-child {
  position: absolute;
  border: 2px solid #fff;
  width: 30px;
  height: 30px;
  left: -16px;
  top: -2px;
  background: transparent;
  border: 2px solid;
  border-color: #fff transparent #fff transparent;
  -webkit-animation: rotate 1s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
  animation: rotate 1s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
}
</style>
