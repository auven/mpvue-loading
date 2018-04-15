<template>
  <div class="ball-grid-beat vue-loaders" :style="{ width: rootStylesWidth }">
    <div v-for="n in 9" :key="n" :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
    <!-- <div :style="styles"></div>
    <div :style="styles"></div>
    <div :style="styles"></div>
    <div :style="styles"></div>
    <div :style="styles"></div>
    <div :style="styles"></div>
    <div :style="styles"></div>
    <div :style="styles"></div> -->
  </div>
</template>

<script>
export default {
  name: 'BallGridBeatLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    rootStylesWidth() {
      return this.size ? `calc(3 * (${this.size || '15px'} + 4px))` : null
    }
  }
}
</script>

<style scoped>
@-webkit-keyframes ball-grid-beat {
  50% {
    opacity: 0.7;
  }
  100% {
    opacity: 1;
  }
}

@keyframes ball-grid-beat {
  50% {
    opacity: 0.7;
  }
  100% {
    opacity: 1;
  }
}

.ball-grid-beat {
  width: 57px;
}
.ball-grid-beat > div:nth-child(1) {
  -webkit-animation-delay: 0.44s;
  animation-delay: 0.44s;
  -webkit-animation-duration: 1.27s;
  animation-duration: 1.27s;
}
.ball-grid-beat > div:nth-child(2) {
  -webkit-animation-delay: 0.2s;
  animation-delay: 0.2s;
  -webkit-animation-duration: 1.52s;
  animation-duration: 1.52s;
}
.ball-grid-beat > div:nth-child(3) {
  -webkit-animation-delay: 0.14s;
  animation-delay: 0.14s;
  -webkit-animation-duration: 0.61s;
  animation-duration: 0.61s;
}
.ball-grid-beat > div:nth-child(4) {
  -webkit-animation-delay: 0.15s;
  animation-delay: 0.15s;
  -webkit-animation-duration: 0.82s;
  animation-duration: 0.82s;
}
.ball-grid-beat > div:nth-child(5) {
  -webkit-animation-delay: -0.01s;
  animation-delay: -0.01s;
  -webkit-animation-duration: 1.24s;
  animation-duration: 1.24s;
}
.ball-grid-beat > div:nth-child(6) {
  -webkit-animation-delay: -0.07s;
  animation-delay: -0.07s;
  -webkit-animation-duration: 1.35s;
  animation-duration: 1.35s;
}
.ball-grid-beat > div:nth-child(7) {
  -webkit-animation-delay: 0.29s;
  animation-delay: 0.29s;
  -webkit-animation-duration: 1.44s;
  animation-duration: 1.44s;
}
.ball-grid-beat > div:nth-child(8) {
  -webkit-animation-delay: 0.63s;
  animation-delay: 0.63s;
  -webkit-animation-duration: 1.19s;
  animation-duration: 1.19s;
}
.ball-grid-beat > div:nth-child(9) {
  -webkit-animation-delay: -0.18s;
  animation-delay: -0.18s;
  -webkit-animation-duration: 1.48s;
  animation-duration: 1.48s;
}
.ball-grid-beat > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  float: left;
  -webkit-animation-name: ball-grid-beat;
  animation-name: ball-grid-beat;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-delay: 0;
  animation-delay: 0;
}
</style>

