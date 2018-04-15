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
        <BallPulse />
      </div>
      <div class="loaders-item">
        <BallPulseSync />
      </div>
      <div class="loaders-item">
        <BallPulseRise />
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
        <BallTrianglePath />
      </div>
      <div class="loaders-item">
        <BallSpinFade />
      </div>
      <div class="loaders-item">
        <BallScale />
      </div>
      <div class="loaders-item">
        <BallScaleRipple />
      </div>
      <div class="loaders-item">
        <BallScaleRippleMultiple />
      </div>
      <div class="loaders-item">
        <BallScaleMultiple />
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
        <BallGridBeat />
      </div>
      <div class="loaders-item">
        <BallGridPulse />
      </div>
      <div class="loaders-item">
        <BallClipRotatePulse />
      </div>
    </div>
  </scroll-view>
</template>

<script>
import BallPulse from '../src/loaders/ball-pulse'
import BallPulseSync from '../src/loaders/ball-pulse-sync'
import BallPulseRise from '../src/loaders/ball-pulse-rise'
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
import BallGridBeat from '../src/loaders/ball-grid-beat'
import BallGridPulse from '../src/loaders/ball-grid-pulse'
import BallClipRotatePulse from '../src/loaders/ball-clip-rotate-pulse'
import BallScaleMultiple from '../src/loaders/ball-scale-multiple'
import BallScaleRippleMultiple from '../src/loaders/ball-scale-ripple-multiple'
import BallScaleRipple from '../src/loaders/ball-scale-ripple'
import BallScale from '../src/loaders/ball-scale'
import BallSpinFade from '../src/loaders/ball-spin-fade'
import BallTrianglePath from '../src/loaders/ball-triangle-path'
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
    BallGridBeat,
    BallGridPulse,
    BallClipRotatePulse,
    BallPulseRise,
    BallPulseSync,
    BallPulse,
    BallScaleMultiple,
    BallScaleRippleMultiple,
    BallScaleRipple,
    BallScale,
    BallSpinFade,
    BallTrianglePath
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
