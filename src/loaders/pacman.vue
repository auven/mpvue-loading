<template>
  <div class="pacman vue-loaders" :style="{
    borderRightWIdth: root_borderRightWidth
  }">
    <div :style="{
      borderWidth: styles_borderWidth,
      borderRadius: styles_borderRadius,
      borderTopColor: color,
      borderLeftColor: color,
      borderBottomColor: color
    }"></div>
    <div :style="{
      borderWidth: styles_borderWidth,
      borderRadius: styles_borderRadius,
      borderTopColor: color,
      borderLeftColor: color,
      borderBottomColor: color,
      marginTop: styles_marginTop
    }"></div>
    <div v-for="n in 3" :key="n" :style="{
      width: circle_width_height,
      height: circle_width_height,
      top: circle_top,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
const CIRCLE_SIZE_RATIO = 10 / 50

export default {
  name: 'PacmanLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    root_borderRightWidth() {
      return this.size
        ? `calc(70px + ${CIRCLE_SIZE_RATIO} * ${this.size} - ${this.size})`
        : null
    },
    styles_marginTop() {
      return `calc(${this.size} * -1)`
    },
    styles_borderWidth() {
      return `calc(${this.size} / 2)`
    },
    styles_borderRadius() {
      return `calc(${this.size} / 2)`
    },
    circle_width_height() {
      return `calc(${this.size} * ${CIRCLE_SIZE_RATIO})`
    },
    circle_top() {
      return `calc(${this.size} * 0.5 + (${
        this.size
      } * ${CIRCLE_SIZE_RATIO}) / -2 + 6.25px)`
    }
  }
}
</script>

<style scoped>
.vue-loaders.pacman {
  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
}

.vue-loaders.pacman > div:nth-child(1n + 3) {
  margin: 0;
}

@-webkit-keyframes rotate_pacman_half_up {
  0% {
    -webkit-transform: rotate(270deg);
    transform: rotate(270deg);
  }
  50% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
  100% {
    -webkit-transform: rotate(270deg);
    transform: rotate(270deg);
  }
}

@keyframes rotate_pacman_half_up {
  0% {
    -webkit-transform: rotate(270deg);
    transform: rotate(270deg);
  }
  50% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
  100% {
    -webkit-transform: rotate(270deg);
    transform: rotate(270deg);
  }
}

@-webkit-keyframes rotate_pacman_half_down {
  0% {
    -webkit-transform: rotate(90deg);
    transform: rotate(90deg);
  }
  50% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(90deg);
    transform: rotate(90deg);
  }
}

@keyframes rotate_pacman_half_down {
  0% {
    -webkit-transform: rotate(90deg);
    transform: rotate(90deg);
  }
  50% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(90deg);
    transform: rotate(90deg);
  }
}

@-webkit-keyframes pacman-balls {
  75% {
    opacity: 0.7;
  }
  100% {
    -webkit-transform: translate(-100px, -6.25px);
    transform: translate(-100px, -6.25px);
  }
}

@keyframes pacman-balls {
  75% {
    opacity: 0.7;
  }
  100% {
    -webkit-transform: translate(-100px, -6.25px);
    transform: translate(-100px, -6.25px);
  }
}

.pacman {
  position: relative;
}
.pacman > div:nth-child(2) {
  -webkit-animation: pacman-balls 1s -0.99s infinite linear;
  animation: pacman-balls 1s -0.99s infinite linear;
}
.pacman > div:nth-child(3) {
  -webkit-animation: pacman-balls 1s -0.66s infinite linear;
  animation: pacman-balls 1s -0.66s infinite linear;
}
.pacman > div:nth-child(4) {
  -webkit-animation: pacman-balls 1s -0.33s infinite linear;
  animation: pacman-balls 1s -0.33s infinite linear;
}
.pacman > div:nth-child(5) {
  -webkit-animation: pacman-balls 1s 0s infinite linear;
  animation: pacman-balls 1s 0s infinite linear;
}
.pacman > div:first-of-type {
  width: 0px;
  height: 0px;
  border-right: 25px solid transparent;
  border-top: 25px solid #fff;
  border-left: 25px solid #fff;
  border-bottom: 25px solid #fff;
  border-radius: 25px;
  -webkit-animation: rotate_pacman_half_up 0.5s 0s infinite;
  animation: rotate_pacman_half_up 0.5s 0s infinite;
  position: relative;
  left: -30px;
}
.pacman > div:nth-child(2) {
  width: 0px;
  height: 0px;
  border-right: 25px solid transparent;
  border-top: 25px solid #fff;
  border-left: 25px solid #fff;
  border-bottom: 25px solid #fff;
  border-radius: 25px;
  -webkit-animation: rotate_pacman_half_down 0.5s 0s infinite;
  animation: rotate_pacman_half_down 0.5s 0s infinite;
  margin-top: -50px;
  position: relative;
  left: -30px;
}
.pacman > div:nth-child(3),
.pacman > div:nth-child(4),
.pacman > div:nth-child(5),
.pacman > div:nth-child(6) {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  width: 10px;
  height: 10px;
  position: absolute;
  -webkit-transform: translate(0, -6.25px);
  -ms-transform: translate(0, -6.25px);
  transform: translate(0, -6.25px);
  top: 25px;
  left: 70px;
}
</style>
