<template>
  <div class="ball-zig-zag-deflect vue-loaders" :style="{
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
  name: 'BallZigZagDeflectLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
.vue-loaders.ball-zig-zag-deflect {
  transform: none;
  height: 15px;
  width: 15px;
  padding: 30px 15px;
}

.vue-loaders.ball-zig-zag-deflect > div {
  left: auto;
  top: auto;
  margin: 0;
}

@-webkit-keyframes ball-zig-deflect {
  17% {
    -webkit-transform: translate(-15px, -30px);
    transform: translate(-15px, -30px);
  }
  34% {
    -webkit-transform: translate(15px, -30px);
    transform: translate(15px, -30px);
  }
  50% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
  67% {
    -webkit-transform: translate(15px, -30px);
    transform: translate(15px, -30px);
  }
  84% {
    -webkit-transform: translate(-15px, -30px);
    transform: translate(-15px, -30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

@keyframes ball-zig-deflect {
  17% {
    -webkit-transform: translate(-15px, -30px);
    transform: translate(-15px, -30px);
  }
  34% {
    -webkit-transform: translate(15px, -30px);
    transform: translate(15px, -30px);
  }
  50% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
  67% {
    -webkit-transform: translate(15px, -30px);
    transform: translate(15px, -30px);
  }
  84% {
    -webkit-transform: translate(-15px, -30px);
    transform: translate(-15px, -30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

@-webkit-keyframes ball-zag-deflect {
  17% {
    -webkit-transform: translate(15px, 30px);
    transform: translate(15px, 30px);
  }
  34% {
    -webkit-transform: translate(-15px, 30px);
    transform: translate(-15px, 30px);
  }
  50% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
  67% {
    -webkit-transform: translate(-15px, 30px);
    transform: translate(-15px, 30px);
  }
  84% {
    -webkit-transform: translate(15px, 30px);
    transform: translate(15px, 30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

@keyframes ball-zag-deflect {
  17% {
    -webkit-transform: translate(15px, 30px);
    transform: translate(15px, 30px);
  }
  34% {
    -webkit-transform: translate(-15px, 30px);
    transform: translate(-15px, 30px);
  }
  50% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
  67% {
    -webkit-transform: translate(-15px, 30px);
    transform: translate(-15px, 30px);
  }
  84% {
    -webkit-transform: translate(15px, 30px);
    transform: translate(15px, 30px);
  }
  100% {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

.ball-zig-zag-deflect {
  position: relative;
  -webkit-transform: translate(-15px, -15px);
  -ms-transform: translate(-15px, -15px);
  transform: translate(-15px, -15px);
}
.ball-zig-zag-deflect > div {
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
.ball-zig-zag-deflect > div:first-child {
  -webkit-animation: ball-zig-deflect 1.5s 0s infinite linear;
  animation: ball-zig-deflect 1.5s 0s infinite linear;
}
.ball-zig-zag-deflect > div:last-child {
  -webkit-animation: ball-zag-deflect 1.5s 0s infinite linear;
  animation: ball-zag-deflect 1.5s 0s infinite linear;
}
</style>
