<template>
  <div class="ball-clip-rotate-multiple vue-loaders" :style="{ width: stylesSize, height: stylesSize }">
    <div :style="{ width: stylesSize, height: stylesSize, borderWidth: ballStylesBdW, top: outerBallStylesTopLeft, left: outerBallStylesTopLeft, borderLeftColor: color, borderRightColor: color }"></div>
    <div :style="{ width: innerBallStylesWH, height: innerBallStylesWH, borderWidth: ballStylesBdW, top: innerBallStylesTopLeft, left: innerBallStylesTopLeft, borderTopColor: color, borderBottomColor: color }"></div>
  </div>
</template>

<script>
const BASE_SIZE_PX = '35px'
const BORDER_RATION = 2 / 35
const INNER_BALL_SIZE_RATION = 15 / 30

export default {
  name: 'BallClipRotateMultipleLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    stylesSize() {
      return this.size ? String(this.size) : BASE_SIZE_PX
    },
    ballStylesBdW() {
      return `calc(${this.stylesSize} * ${BORDER_RATION})`
    },
    outerBallStylesTopLeft() {
      return `calc(${this.stylesSize} * -1 * ${BORDER_RATION})`
    },
    innerBallStylesWH() {
      return `calc(${this.stylesSize} * ${INNER_BALL_SIZE_RATION})`
    },
    innerBallStylesTopLeft() {
      return `calc(${this.stylesSize} * -1 * ${BORDER_RATION} + ${
        this.stylesSize
      } / 4.5)`
    }
  }
}
</script>

<style>
/* .vue-loaders.ball-clip-rotate-multiple > div,
.vue-loaders.ball-clip-rotate-multiple > div:last-child {
  left: auto;
  top: auto;
} */
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

.ball-clip-rotate-multiple {
  position: relative;
}
.ball-clip-rotate-multiple > div {
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  left: -20px;
  top: -20px;
  border: 2px solid #fff;
  border-bottom-color: transparent;
  border-top-color: transparent;
  border-radius: 100%;
  height: 35px;
  width: 35px;
  -webkit-animation: rotate 1s 0s ease-in-out infinite;
  animation: rotate 1s 0s ease-in-out infinite;
}
.ball-clip-rotate-multiple > div:last-child {
  display: inline-block;
  top: -10px;
  left: -10px;
  width: 15px;
  height: 15px;
  -webkit-animation-duration: 0.5s;
  animation-duration: 0.5s;
  border-color: #fff transparent #fff transparent;
  -webkit-animation-direction: reverse;
  animation-direction: reverse;
}
</style>
