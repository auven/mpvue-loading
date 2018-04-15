<template>
  <div class="line-scale vue-loaders">
    <div v-for="n in 5" :key="n" :style="{
      width: styles_width,
      height: size,
      borderRadius: styles_borderRadius,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
const WIDTH_RATIO = 4 / 35
const BORDER_RATIO = 2 / 4

export default {
  name: 'LineScaleLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    styles_width() {
      return `calc(${this.size} * ${WIDTH_RATIO})`
    },
    styles_borderRadius() {
      return `calc(${this.size} * ${BORDER_RATIO})`
    }
  }
}
</script>

<style scoped>
@-webkit-keyframes line-scale {
  0% {
    -webkit-transform: scaley(1);
    transform: scaley(1);
  }
  50% {
    -webkit-transform: scaley(0.4);
    transform: scaley(0.4);
  }
  100% {
    -webkit-transform: scaley(1);
    transform: scaley(1);
  }
}
@keyframes line-scale {
  0% {
    -webkit-transform: scaley(1);
    transform: scaley(1);
  }
  50% {
    -webkit-transform: scaley(0.4);
    transform: scaley(0.4);
  }
  100% {
    -webkit-transform: scaley(1);
    transform: scaley(1);
  }
}

.line-scale > div:nth-child(1) {
  -webkit-animation: line-scale 1s -0.4s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: line-scale 1s -0.4s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.line-scale > div:nth-child(2) {
  -webkit-animation: line-scale 1s -0.3s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: line-scale 1s -0.3s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.line-scale > div:nth-child(3) {
  -webkit-animation: line-scale 1s -0.2s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: line-scale 1s -0.2s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.line-scale > div:nth-child(4) {
  -webkit-animation: line-scale 1s -0.1s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: line-scale 1s -0.1s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.line-scale > div:nth-child(5) {
  -webkit-animation: line-scale 1s 0s infinite
    cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: line-scale 1s 0s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.line-scale > div {
  background-color: #fff;
  width: 4px;
  height: 35px;
  border-radius: 2px;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
}
</style>

