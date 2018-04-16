# mpvue-loading

适用于 mpvue 的加载动画插件。基于 vue 版的 [loaders.css](https://github.com/ConnorAtherton/loaders.css) 开源库 [vue-loaders](https://github.com/Hokid/vue-loaders) 进行修改，将其中的样式绑定由`styleObject`语法修改成单一属性绑定。

## 使用方式

首先是安装
```
npm install mpvue-loading -S
```

在项目中使用
```
import BallPulse from 'mpvue-loading/src/loaders/ball-pulse'

export default {
  components: {
    BallPulse
  }
}
```

详情参考 [example](example/index.vue)
