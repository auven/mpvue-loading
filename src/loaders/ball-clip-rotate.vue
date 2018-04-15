<template>
  <div class="ball-clip-rotate vue-loaders">
    <div :style="{
      width: size,
      height: size,
      borderWidth: borderWidth,
      borderTopColor: color,
      borderRightColor: color,
      borderLeftColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'BallClipRotateLoader',
  props: {
    size: String,
    color: String
  },
  data() {
    return {
      BORDER_RATION: 2 / 15
    }
  },
  computed: {
    borderWidth() {
      return `calc(${this.size} * ${this.BORDER_RATION})`
    }
  }
}
</script>

<style scoped>
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

.ball-clip-rotate > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  border: 2px solid #fff;
  border-bottom-color: transparent;
  height: 25px;
  width: 25px;
  background: transparent !important;
  display: inline-block;
  -webkit-animation: rotate 0.75s 0s linear infinite;
  animation: rotate 0.75s 0s linear infinite;
}
</style>

