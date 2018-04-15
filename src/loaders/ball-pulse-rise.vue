<template>
  <div class="ball-pulse-rise vue-loaders">
    <div v-for="n in 5" :key="n" :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'BallPulseRiseLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
.vue-loaders.ball-pulse-rise {
  padding-top: 30px;
  padding-bottom: 30px;
}
@-webkit-keyframes ball-pulse-rise-even {
  0% {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
  25% {
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  50% {
    -webkit-transform: scale(0.4);
    transform: scale(0.4);
  }
  75% {
    -webkit-transform: translateY(30px);
    transform: translateY(30px);
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@keyframes ball-pulse-rise-even {
  0% {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
  25% {
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  50% {
    -webkit-transform: scale(0.4);
    transform: scale(0.4);
  }
  75% {
    -webkit-transform: translateY(30px);
    transform: translateY(30px);
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@-webkit-keyframes ball-pulse-rise-odd {
  0% {
    -webkit-transform: scale(0.4);
    transform: scale(0.4);
  }
  25% {
    -webkit-transform: translateY(30px);
    transform: translateY(30px);
  }
  50% {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
  75% {
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-transform: scale(0.75);
    transform: scale(0.75);
  }
}

@keyframes ball-pulse-rise-odd {
  0% {
    -webkit-transform: scale(0.4);
    transform: scale(0.4);
  }
  25% {
    -webkit-transform: translateY(30px);
    transform: translateY(30px);
  }
  50% {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
  75% {
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-transform: scale(0.75);
    transform: scale(0.75);
  }
}

.ball-pulse-rise > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-timing-function: cubic-bezier(0.15, 0.46, 0.9, 0.6);
  animation-timing-function: cubic-bezier(0.15, 0.46, 0.9, 0.6);
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-delay: 0;
  animation-delay: 0;
}
.ball-pulse-rise > div:nth-child(2n) {
  -webkit-animation-name: ball-pulse-rise-even;
  animation-name: ball-pulse-rise-even;
}
.ball-pulse-rise > div:nth-child(2n-1) {
  -webkit-animation-name: ball-pulse-rise-odd;
  animation-name: ball-pulse-rise-odd;
}
</style>
