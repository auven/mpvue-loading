<template>
  <div class="semi-circle-spin vue-loaders" :style="{
    width: size,
    height: size
  }">
    <div :style="{
      backgroundImage: styles_backgroundImage
    }"></div>
  </div>
</template>

<script>
export default {
  name: 'SemiCircleSpinLoader',
  props: {
    size: String,
    color: String
  },
  computed: {
    styles_backgroundImage() {
      return `linear-gradient(transparent 0,transparent 70%,${this.color} 30%,${this.color} 100%)`
    }
  }
}
</script>

<style scoped>
@-webkit-keyframes spin-rotate {
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

@keyframes spin-rotate {
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

.semi-circle-spin {
  position: relative;
  width: 35px;
  height: 35px;
  overflow: hidden;
}
.semi-circle-spin > div {
  position: absolute;
  border-width: 0px;
  border-radius: 100%;
  -webkit-animation: spin-rotate 0.6s 0s infinite linear;
  animation: spin-rotate 0.6s 0s infinite linear;
  background-image: -webkit-linear-gradient(
    transparent 0%,
    transparent 70%,
    #fff 30%,
    #fff 100%
  );
  background-image: linear-gradient(
    transparent 0%,
    transparent 70%,
    #fff 30%,
    #fff 100%
  );
  width: 100%;
  height: 100%;
}
</style>

