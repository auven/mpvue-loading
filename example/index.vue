<template>
  <scroll-view class="body" scroll-y>
    <div class="about">
      <div class="about-title">mpvue-loading</div>
      <div class="about-desc">
        适用于 mpvue 的加载动画插件。项目地址：https://github.com/auven/mpvue-loading
      </div>
    </div>
    <div class="loaders">
      <div class="loaders-item">
        <BallPulseLoader />
      </div>
      <div class="loaders-item">
        <BallPulseSyncLoader />
      </div>
      <div class="loaders-item">
        <BallPulseRiseLoader />
      </div>
      <div class="loaders-item">
        <BallRotateLoader />
      </div>
      <div class="loaders-item">
        <TriangleSkewSpinLoader />
      </div>
      <div class="loaders-item">
        <SquareSpinLoader />
      </div>
      <div class="loaders-item">
        <SemiCircleSpinLoader />
      </div>
      <div class="loaders-item">
        <PacmanLoader />
      </div>
      <div class="loaders-item">
        <LineSpinFadeLoader />
      </div>
      <div class="loaders-item">
        <LineScaleLoader />
      </div>
      <div class="loaders-item">
        <LineScalePulseOutLoader />
      </div>
      <div class="loaders-item">
        <LineScalePulseOutRapidLoader />
      </div>
      <div class="loaders-item">
        <LineScalePartyLoader />
      </div>
      <div class="loaders-item">
        <CubeTransitionLoader />
      </div>
      <div class="loaders-item">
        <BallZigZagLoader />
      </div>
      <div class="loaders-item">
        <BallZigZagDeflectLoader />
      </div>
      <div class="loaders-item">
        <BallTrianglePathLoader />
      </div>
      <div class="loaders-item">
        <BallSpinFadeLoader />
      </div>
      <div class="loaders-item">
        <BallScaleLoader />
      </div>
      <div class="loaders-item">
        <BallScaleRippleLoader />
      </div>
      <div class="loaders-item">
        <BallScaleRippleMultipleLoader />
      </div>
      <div class="loaders-item">
        <BallScaleMultipleLoader />
      </div>

      <div class="loaders-item">
        <BallBeatLoader />
      </div>
      <div class="loaders-item">
        <BallClipRotateMultipleLoader />
      </div>
      <div class="loaders-item">
        <BallClipRotateLoader />
      </div>
      <div class="loaders-item">
        <BallGridBeatLoader />
      </div>
      <div class="loaders-item">
        <BallGridPulseLoader />
      </div>
      <div class="loaders-item">
        <BallClipRotatePulseLoader />
      </div>
    </div>
  </scroll-view>
</template>

<script>
import BallPulseLoader from '../src/loaders/ball-pulse'
import BallPulseSyncLoader from '../src/loaders/ball-pulse-sync'
import BallPulseRiseLoader from '../src/loaders/ball-pulse-rise'
import BallRotateLoader from '../src/loaders/ball-rotate'
import TriangleSkewSpinLoader from '../src/loaders/triangle-skew-spin'
import SquareSpinLoader from '../src/loaders/square-spin'
import SemiCircleSpinLoader from '../src/loaders/semi-circle-spin'
import PacmanLoader from '../src/loaders/pacman'
import LineSpinFadeLoader from '../src/loaders/line-spin-fade'
import LineScaleLoader from '../src/loaders/line-scale'
import LineScalePulseOutLoader from '../src/loaders/line-scale-pulse-out'
import LineScalePulseOutRapidLoader from '../src/loaders/line-scale-pulse-out-rapid'
import LineScalePartyLoader from '../src/loaders/line-scale-party'
import CubeTransitionLoader from '../src/loaders/cube-transition'
import BallZigZagLoader from '../src/loaders/ball-zig-zag'
import BallZigZagDeflectLoader from '../src/loaders/ball-zig-zag-deflect'
import BallBeatLoader from '../src/loaders/ball-beat'
import BallClipRotateMultipleLoader from '../src/loaders/ball-clip-rotate-multiple'
import BallClipRotateLoader from '../src/loaders/ball-clip-rotate'
import BallGridBeatLoader from '../src/loaders/ball-grid-beat'
import BallGridPulseLoader from '../src/loaders/ball-grid-pulse'
import BallClipRotatePulseLoader from '../src/loaders/ball-clip-rotate-pulse'
import BallScaleMultipleLoader from '../src/loaders/ball-scale-multiple'
import BallScaleRippleMultipleLoader from '../src/loaders/ball-scale-ripple-multiple'
import BallScaleRippleLoader from '../src/loaders/ball-scale-ripple'
import BallScaleLoader from '../src/loaders/ball-scale'
import BallSpinFadeLoader from '../src/loaders/ball-spin-fade'
import BallTrianglePathLoader from '../src/loaders/ball-triangle-path'
export default {
  components: {
    BallRotateLoader,
    TriangleSkewSpinLoader,
    SquareSpinLoader,
    SemiCircleSpinLoader,
    PacmanLoader,
    LineSpinFadeLoader,
    LineScaleLoader,
    LineScalePulseOutLoader,
    LineScalePulseOutRapidLoader,
    LineScalePartyLoader,
    CubeTransitionLoader,
    BallZigZagLoader,
    BallZigZagDeflectLoader,
    BallBeatLoader,
    BallClipRotateMultipleLoader,
    BallClipRotateLoader,
    BallGridBeatLoader,
    BallGridPulseLoader,
    BallClipRotatePulseLoader,
    BallPulseRiseLoader,
    BallPulseSyncLoader,
    BallPulseLoader,
    BallScaleMultipleLoader,
    BallScaleRippleMultipleLoader,
    BallScaleRippleLoader,
    BallScaleLoader,
    BallSpinFadeLoader,
    BallTrianglePathLoader
  }
}
</script>

<style>
.body {
  background: #ed5565;
}
.about {
  padding: 60rpx;
  color: #fff;
}
.about .about-title {
  font-size: 48rpx;
  font-weight: 600;
  margin-bottom: 20rpx;
}
.about .about-desc {
  font-size: 28rpx;
}
.loaders {
  display: flex;
  flex-wrap: wrap;
}
.loaders-item {
  box-sizing: border-box;
  width: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 25% 0;
}
</style>
