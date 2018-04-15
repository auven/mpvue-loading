<template>
  <div class="ball-rotate vue-loaders" :style="{
    width: size,
    height: size,
    padding: rootStyles_padding
  }">
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color
    }">
      <div :style="{
        width: size,
        height: size,
        backgroundColor: color,
        left: innerLeft
      }"></div>
      <div :style="{
        width: size,
        height: size,
        backgroundColor: color,
        right: innerRight
      }"></div>
    </div>
  </div>
</template>

<script>
const OFFSET = 10 / 15

export default {
  name: 'BallRotateLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    rootStyles_padding() {
      return `calc(${this.size} + ${this.size} * ${OFFSET} + 2px)`
    },
    innerLeft() {
      return `calc((${this.size} + ${this.size} * ${OFFSET} + 2px) * -1)`
    },
    innerRight() {
      return `calc(${this.size} + ${this.size} * ${OFFSET} + 2px)`
    }
  }
}
</script>

<style scoped>
.vue-loaders.ball-rotate > div:before,
.vue-loaders.ball-rotate > div:after {
  display: none;
}

.vue-loaders.ball-rotate {
  padding: 26px;
}

.vue-loaders.ball-rotate > div {
  margin: 0;
}

.vue-loaders.ball-rotate > div > div {
  top: auto;
  position: absolute;
  opacity: 0.8;
  background-color: #ffffff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
}

.vue-loaders.ball-rotate > div > div:first-child {
  left: -26px;
}

.vue-loaders.ball-rotate > div > div:last-child {
  left: 26px;
}

@-webkit-keyframes rotate {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  50% {
    -webkit-transform: rotate(180deg);
    transform: rotate(180deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}

@keyframes rotate {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  50% {
    -webkit-transform: rotate(180deg);
    transform: rotate(180deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}

.ball-rotate {
  position: relative;
}
.ball-rotate > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: relative;
}
.ball-rotate > div:first-child {
  -webkit-animation: rotate 1s 0s cubic-bezier(0.7, -0.13, 0.22, 0.86) infinite;
  animation: rotate 1s 0s cubic-bezier(0.7, -0.13, 0.22, 0.86) infinite;
}
.ball-rotate > div:before,
.ball-rotate > div:after {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  content: '';
  position: absolute;
  opacity: 0.8;
}
.ball-rotate > div:before {
  top: 0px;
  left: -28px;
}
.ball-rotate > div:after {
  top: 0px;
  left: 25px;
}
</style>
