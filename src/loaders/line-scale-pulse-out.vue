<template>
  <div class="line-scale-pulse-out vue-loaders">
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
  name: 'LineScalePulseOutLoader',
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
@-webkit-keyframes line-scale-pulse-out {
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

@keyframes line-scale-pulse-out {
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

.line-scale-pulse-out > div {
  background-color: #fff;
  width: 4px;
  height: 35px;
  border-radius: 2px;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  -webkit-animation: line-scale-pulse-out 0.9s -0.6s infinite cubic-bezier(0.85, 0.25, 0.37, 0.85);
  animation: line-scale-pulse-out 0.9s -0.6s infinite cubic-bezier(0.85, 0.25, 0.37, 0.85);
}
.line-scale-pulse-out > div:nth-child(2),
.line-scale-pulse-out > div:nth-child(4) {
  -webkit-animation-delay: -0.4s !important;
  animation-delay: -0.4s !important;
}
.line-scale-pulse-out > div:nth-child(1),
.line-scale-pulse-out > div:nth-child(5) {
  -webkit-animation-delay: -0.2s !important;
  animation-delay: -0.2s !important;
}
</style>

