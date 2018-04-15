<template>
  <div class="square-spin vue-loaders">
    <div :style="{
      width: size,
      height: size,
      backgroundColor: color
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'SquareSpinLoader',
  props: {
    size: String,
    color: String
  }
}
</script>

<style scoped>
.vue-loaders.square-spin > div {
  border: 0;
}

@-webkit-keyframes square-spin {
  25% {
    -webkit-transform: perspective(100px) rotateX(180deg) rotateY(0);
    transform: perspective(100px) rotateX(180deg) rotateY(0);
  }
  50% {
    -webkit-transform: perspective(100px) rotateX(180deg) rotateY(180deg);
    transform: perspective(100px) rotateX(180deg) rotateY(180deg);
  }
  75% {
    -webkit-transform: perspective(100px) rotateX(0) rotateY(180deg);
    transform: perspective(100px) rotateX(0) rotateY(180deg);
  }
  100% {
    -webkit-transform: perspective(100px) rotateX(0) rotateY(0);
    transform: perspective(100px) rotateX(0) rotateY(0);
  }
}

@keyframes square-spin {
  25% {
    -webkit-transform: perspective(100px) rotateX(180deg) rotateY(0);
    transform: perspective(100px) rotateX(180deg) rotateY(0);
  }
  50% {
    -webkit-transform: perspective(100px) rotateX(180deg) rotateY(180deg);
    transform: perspective(100px) rotateX(180deg) rotateY(180deg);
  }
  75% {
    -webkit-transform: perspective(100px) rotateX(0) rotateY(180deg);
    transform: perspective(100px) rotateX(0) rotateY(180deg);
  }
  100% {
    -webkit-transform: perspective(100px) rotateX(0) rotateY(0);
    transform: perspective(100px) rotateX(0) rotateY(0);
  }
}

.square-spin > div {
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  width: 50px;
  height: 50px;
  background: #fff;
  border: 1px solid red;
  -webkit-animation: square-spin 3s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9)
    infinite;
  animation: square-spin 3s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
}
</style>
