<template>
  <div class="ball-scale-ripple-multiple vue-loaders" :style="{
    width: rootStyleWH,
    height: rootStyleWH
  }">
    <div v-for="n in 3" :key="n" :style="{
      width: size,
      height: size,
      borderColor: color,
      borderWidth: stylesBorderWidth
    }"></div>
  </div>
</template>

<script>
const BORDER_RATION = 2 / 50

export default {
  name: 'BallScaleRippleMultipleLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    rootStyleWH() {
      return `calc(${this.size} + ${this.size} * ${BORDER_RATION})`
    },
    stylesBorderWidth() {
      return `calc(${this.size} * ${BORDER_RATION})`
    }
  }
}
</script>

<style scoped>
.vue-loaders.ball-scale-ripple-multiple {
  transform: none;
  width: 54px;
  height: 54px;
}

.vue-loaders.ball-scale-ripple-multiple > div {
  top: auto;
  left: auto;
}

@-webkit-keyframes ball-scale-ripple-multiple {
  0% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 1;
  }
  70% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0.7;
  }
  100% {
    opacity: 0;
  }
}

@keyframes ball-scale-ripple-multiple {
  0% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 1;
  }
  70% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0.7;
  }
  100% {
    opacity: 0;
  }
}

.ball-scale-ripple-multiple {
  position: relative;
  -webkit-transform: translateY(-25px);
  -ms-transform: translateY(-25px);
  transform: translateY(-25px);
}
.ball-scale-ripple-multiple > div:nth-child(0) {
  -webkit-animation-delay: -0.8s;
  animation-delay: -0.8s;
}
.ball-scale-ripple-multiple > div:nth-child(1) {
  -webkit-animation-delay: -0.6s;
  animation-delay: -0.6s;
}
.ball-scale-ripple-multiple > div:nth-child(2) {
  -webkit-animation-delay: -0.4s;
  animation-delay: -0.4s;
}
.ball-scale-ripple-multiple > div:nth-child(3) {
  -webkit-animation-delay: -0.2s;
  animation-delay: -0.2s;
}
.ball-scale-ripple-multiple > div {
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  top: -2px;
  left: -26px;
  width: 50px;
  height: 50px;
  border-radius: 100%;
  border: 2px solid #fff;
  -webkit-animation: ball-scale-ripple-multiple 1.25s 0s infinite
    cubic-bezier(0.21, 0.53, 0.56, 0.8);
  animation: ball-scale-ripple-multiple 1.25s 0s infinite
    cubic-bezier(0.21, 0.53, 0.56, 0.8);
}
</style>
