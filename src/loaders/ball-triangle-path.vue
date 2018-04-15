<template>
  <div class="ball-triangle-path vue-loaders" :style="{
    width: rootStyle_width_height,
    heigth: rootStyle_width_height
  }">
    <div v-for="n in 3" :key="n" :style="{
      width: size,
      height: size,
      borderColor: color,
      borderWidth: styles_borderWidth
    }"></div>
  </div>
</template>

<script>
const BORDER_RATION = 1 / 10

export default {
  name: 'BallTrianglePathLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    rootStyle_width_height() {
      return `calc(${this.size} + 50px)`
    },
    styles_borderWidth() {
      return `calc(${this.size} * ${BORDER_RATION})`
    }
  }
}
</script>

<style scoped>
.vue-loaders.ball-triangle-path {
  transform: none;
  width: 60px;
  height: 60px;
}

@-webkit-keyframes ball-triangle-path-1 {
  33% {
    -webkit-transform: translate(25px, -50px);
    transform: translate(25px, -50px);
  }
  66% {
    -webkit-transform: translate(50px, 0px);
    transform: translate(50px, 0px);
  }
  100% {
    -webkit-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }
}

@keyframes ball-triangle-path-1 {
  33% {
    -webkit-transform: translate(25px, -50px);
    transform: translate(25px, -50px);
  }
  66% {
    -webkit-transform: translate(50px, 0px);
    transform: translate(50px, 0px);
  }
  100% {
    -webkit-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }
}

@-webkit-keyframes ball-triangle-path-2 {
  33% {
    -webkit-transform: translate(25px, 50px);
    transform: translate(25px, 50px);
  }
  66% {
    -webkit-transform: translate(-25px, 50px);
    transform: translate(-25px, 50px);
  }
  100% {
    -webkit-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }
}

@keyframes ball-triangle-path-2 {
  33% {
    -webkit-transform: translate(25px, 50px);
    transform: translate(25px, 50px);
  }
  66% {
    -webkit-transform: translate(-25px, 50px);
    transform: translate(-25px, 50px);
  }
  100% {
    -webkit-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }
}

@-webkit-keyframes ball-triangle-path-3 {
  33% {
    -webkit-transform: translate(-50px, 0px);
    transform: translate(-50px, 0px);
  }
  66% {
    -webkit-transform: translate(-25px, -50px);
    transform: translate(-25px, -50px);
  }
  100% {
    -webkit-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }
}

@keyframes ball-triangle-path-3 {
  33% {
    -webkit-transform: translate(-50px, 0px);
    transform: translate(-50px, 0px);
  }
  66% {
    -webkit-transform: translate(-25px, -50px);
    transform: translate(-25px, -50px);
  }
  100% {
    -webkit-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }
}

.ball-triangle-path {
  position: relative;
  -webkit-transform: translate(-29.994px, -37.50938px);
  -ms-transform: translate(-29.994px, -37.50938px);
  transform: translate(-29.994px, -37.50938px);
}
.ball-triangle-path > div:nth-child(1) {
  -webkit-animation-name: ball-triangle-path-1;
  animation-name: ball-triangle-path-1;
  -webkit-animation-delay: 0;
  animation-delay: 0;
  -webkit-animation-duration: 2s;
  animation-duration: 2s;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
}
.ball-triangle-path > div:nth-child(2) {
  -webkit-animation-name: ball-triangle-path-2;
  animation-name: ball-triangle-path-2;
  -webkit-animation-delay: 0;
  animation-delay: 0;
  -webkit-animation-duration: 2s;
  animation-duration: 2s;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
}
.ball-triangle-path > div:nth-child(3) {
  -webkit-animation-name: ball-triangle-path-3;
  animation-name: ball-triangle-path-3;
  -webkit-animation-delay: 0;
  animation-delay: 0;
  -webkit-animation-duration: 2s;
  animation-duration: 2s;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
}
.ball-triangle-path > div {
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  width: 10px;
  height: 10px;
  border-radius: 100%;
  border: 1px solid #fff;
}
.ball-triangle-path > div:nth-of-type(1) {
  top: 50px;
}
.ball-triangle-path > div:nth-of-type(2) {
  left: 25px;
}
.ball-triangle-path > div:nth-of-type(3) {
  top: 50px;
  left: 50px;
}
</style>
