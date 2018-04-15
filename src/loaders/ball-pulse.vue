<template>
  <div class="ball-pulse vue-loaders">
    <div v-for="n in 3" :key="n" :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'BallPulseLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
@-webkit-keyframes scale {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
  45% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 0.7;
  }
  80% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
}
@keyframes scale {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
  45% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 0.7;
  }
  80% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
}

.ball-pulse > div:nth-child(0) {
  -webkit-animation: scale 0.75s -0.36s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: scale 0.75s -0.36s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.ball-pulse > div:nth-child(1) {
  -webkit-animation: scale 0.75s -0.24s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: scale 0.75s -0.24s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.ball-pulse > div:nth-child(2) {
  -webkit-animation: scale 0.75s -0.12s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: scale 0.75s -0.12s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.ball-pulse > div:nth-child(3) {
  -webkit-animation: scale 0.75s 0s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
  animation: scale 0.75s 0s infinite cubic-bezier(0.2, 0.68, 0.18, 1.08);
}

.ball-pulse > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
}
</style>

