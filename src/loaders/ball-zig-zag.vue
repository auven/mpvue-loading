<template>
  <div class="ball-zig-zag vue-loaders" :style="{
    width: size,
    height: size
  }">
    <div v-for="n in 2" :key="n" :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'BallZigZagLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
.vue-loaders.ball-zig-zag {
  transform: none;
  height: 15px;
  width: 15px;
  padding: 30px 15px;
}

.vue-loaders.ball-zig-zag > div {
  left: auto;
  top: auto;
  margin: 0;
}

@-webkit-keyframes ball-zig {
  33% {
    -webkit-transform: translate(-15px, -30px);
    transform: translate(-15px, -30px);
  }
  66% {
    -webkit-transform: translate(15px, -30px);
    transform: translate(15px, -30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

@keyframes ball-zig {
  33% {
    -webkit-transform: translate(-15px, -30px);
    transform: translate(-15px, -30px);
  }
  66% {
    -webkit-transform: translate(15px, -30px);
    transform: translate(15px, -30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

@-webkit-keyframes ball-zag {
  33% {
    -webkit-transform: translate(15px, 30px);
    transform: translate(15px, 30px);
  }
  66% {
    -webkit-transform: translate(-15px, 30px);
    transform: translate(-15px, 30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

@keyframes ball-zag {
  33% {
    -webkit-transform: translate(15px, 30px);
    transform: translate(15px, 30px);
  }
  66% {
    -webkit-transform: translate(-15px, 30px);
    transform: translate(-15px, 30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

.ball-zig-zag {
  position: relative;
  -webkit-transform: translate(-15px, -15px);
  -ms-transform: translate(-15px, -15px);
  transform: translate(-15px, -15px);
}
.ball-zig-zag > div {
  background-color: #fff;
  width: 15px;
  height: 15px;
  border-radius: 100%;
  margin: 2px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  position: absolute;
  margin-left: 15px;
  top: 4px;
  left: -7px;
}
.ball-zig-zag > div:first-child {
  -webkit-animation: ball-zig 0.7s 0s infinite linear;
  animation: ball-zig 0.7s 0s infinite linear;
}
.ball-zig-zag > div:last-child {
  -webkit-animation: ball-zag 0.7s 0s infinite linear;
  animation: ball-zag 0.7s 0s infinite linear;
}
</style>
