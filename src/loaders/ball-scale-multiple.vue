<template>
  <div class="ball-scale-multiple vue-loaders" :style="{
    width: size,
    height: size
  }">
    <div v-for="n in 3" :key="n" :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'BallScaleMultipleLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
.vue-loaders.ball-scale-multiple {
  transform: none;
  width: 60px;
  height: 60px;
}

.vue-loaders.ball-scale-multiple > div {
  top: auto;
  left: auto;
}

@-webkit-keyframes ball-scale-multiple {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
    opacity: 0;
  }
  5% {
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}

@keyframes ball-scale-multiple {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
    opacity: 0;
  }
  5% {
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}

.ball-scale-multiple {
  position: relative;
  -webkit-transform: translateY(-30px);
  -ms-transform: translateY(-30px);
  transform: translateY(-30px);
}
.ball-scale-multiple > div:nth-child(2) {
  -webkit-animation-delay: -0.4s;
  animation-delay: -0.4s;
}
.ball-scale-multiple > div:nth-child(3) {
  -webkit-animation-delay: -0.2s;
  animation-delay: -0.2s;
}
.ball-scale-multiple > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  left: -30px;
  top: 0px;
  opacity: 0;
  margin: 0;
  width: 60px;
  height: 60px;
  -webkit-animation: ball-scale-multiple 1s 0s linear infinite;
  animation: ball-scale-multiple 1s 0s linear infinite;
}
</style>
