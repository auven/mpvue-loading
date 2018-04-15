<template>
  <div class="ball-grid-pulse vue-loaders" :style="{ width: rootStylesWidth }">
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
  name: 'BallGridPulseLoader',
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
.vue-loaders.ball-grid-pulse:before,
.vue-loaders.ball-grid-pulse:after {
  content: '';
  display: table;
}

.vue-loaders.ball-grid-pulse:after {
  clear: both;
}
@-webkit-keyframes ball-grid-pulse {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  50% {
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
    opacity: 0.7;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
}

@keyframes ball-grid-pulse {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  50% {
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
    opacity: 0.7;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
}

.ball-grid-pulse {
  width: 57px;
}
.ball-grid-pulse > div:nth-child(1) {
  -webkit-animation-delay: 0.58s;
  animation-delay: 0.58s;
  -webkit-animation-duration: 0.9s;
  animation-duration: 0.9s;
}
.ball-grid-pulse > div:nth-child(2) {
  -webkit-animation-delay: 0.01s;
  animation-delay: 0.01s;
  -webkit-animation-duration: 0.94s;
  animation-duration: 0.94s;
}
.ball-grid-pulse > div:nth-child(3) {
  -webkit-animation-delay: 0.25s;
  animation-delay: 0.25s;
  -webkit-animation-duration: 1.43s;
  animation-duration: 1.43s;
}
.ball-grid-pulse > div:nth-child(4) {
  -webkit-animation-delay: -0.03s;
  animation-delay: -0.03s;
  -webkit-animation-duration: 0.74s;
  animation-duration: 0.74s;
}
.ball-grid-pulse > div:nth-child(5) {
  -webkit-animation-delay: 0.21s;
  animation-delay: 0.21s;
  -webkit-animation-duration: 0.68s;
  animation-duration: 0.68s;
}
.ball-grid-pulse > div:nth-child(6) {
  -webkit-animation-delay: 0.25s;
  animation-delay: 0.25s;
  -webkit-animation-duration: 1.17s;
  animation-duration: 1.17s;
}
.ball-grid-pulse > div:nth-child(7) {
  -webkit-animation-delay: 0.46s;
  animation-delay: 0.46s;
  -webkit-animation-duration: 1.41s;
  animation-duration: 1.41s;
}
.ball-grid-pulse > div:nth-child(8) {
  -webkit-animation-delay: 0.02s;
  animation-delay: 0.02s;
  -webkit-animation-duration: 1.56s;
  animation-duration: 1.56s;
}
.ball-grid-pulse > div:nth-child(9) {
  -webkit-animation-delay: 0.13s;
  animation-delay: 0.13s;
  -webkit-animation-duration: 0.78s;
  animation-duration: 0.78s;
}
.ball-grid-pulse > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  float: left;
  -webkit-animation-name: ball-grid-pulse;
  animation-name: ball-grid-pulse;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-delay: 0;
  animation-delay: 0;
}
</style>
