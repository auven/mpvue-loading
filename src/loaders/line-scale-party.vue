<template>
  <div class="line-scale-party vue-loaders">
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
  name: 'LineScalePartyLoader',
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
@-webkit-keyframes line-scale-party {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  50% {
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@keyframes line-scale-party {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  50% {
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

.line-scale-party > div:nth-child(1) {
  -webkit-animation-delay: -0.09s;
  animation-delay: -0.09s;
  -webkit-animation-duration: 0.83s;
  animation-duration: 0.83s;
}

.line-scale-party > div:nth-child(2) {
  -webkit-animation-delay: 0.33s;
  animation-delay: 0.33s;
  -webkit-animation-duration: 0.64s;
  animation-duration: 0.64s;
}

.line-scale-party > div:nth-child(3) {
  -webkit-animation-delay: 0.32s;
  animation-delay: 0.32s;
  -webkit-animation-duration: 0.39s;
  animation-duration: 0.39s;
}

.line-scale-party > div:nth-child(4) {
  -webkit-animation-delay: 0.47s;
  animation-delay: 0.47s;
  -webkit-animation-duration: 0.52s;
  animation-duration: 0.52s;
}

.line-scale-party > div {
  background-color: #fff;
  width: 4px;
  height: 35px;
  border-radius: 2px;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  -webkit-animation-name: line-scale-party;
  animation-name: line-scale-party;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-delay: 0;
  animation-delay: 0;
}
</style>

