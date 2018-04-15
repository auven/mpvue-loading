<template>
  <div class="ball-scale vue-loaders">
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'BallScaleLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
@-webkit-keyframes ball-scale {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}

@keyframes ball-scale {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}

.ball-scale > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  height: 60px;
  width: 60px;
  -webkit-animation: ball-scale 1s 0s ease-in-out infinite;
  animation: ball-scale 1s 0s ease-in-out infinite;
}

@keyframes ball-scale {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
  }
}

.ball-scale > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  display: inline-block;
  height: 60px;
  width: 60px;
  -webkit-animation: ball-scale 1s 0s ease-in-out infinite;
  animation: ball-scale 1s 0s ease-in-out infinite;
}

.ball-scale-random {
  width: 37px;
  height: 40px;
}
.ball-scale-random > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  display: inline-block;
  height: 30px;
  width: 30px;
  -webkit-animation: ball-scale 1s 0s ease-in-out infinite;
  animation: ball-scale 1s 0s ease-in-out infinite;
}
.ball-scale-random > div:nth-child(1) {
  margin-left: -7px;
  -webkit-animation: ball-scale 1s 0.2s ease-in-out infinite;
  animation: ball-scale 1s 0.2s ease-in-out infinite;
}
.ball-scale-random > div:nth-child(3) {
  margin-left: -2px;
  margin-top: 9px;
  -webkit-animation: ball-scale 1s 0.5s ease-in-out infinite;
  animation: ball-scale 1s 0.5s ease-in-out infinite;
}
</style>

