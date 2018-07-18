# mpvue_canvas_drawer

把 `mp_canvas_drawer` 组件移动到 `mpvue` 项目的 `/static/` 目录下

在调用页面的 `main.js` 文件最后加入如下代码

```
export default {
  config: {
    // 这儿添加要用的小程序组件
    usingComponents: {
      'canvasdrawer': '../../../static/canvasdrawer/canvasdrawer'
    }
  }
}
```

就可以直接在 `mpvue` 中使用 `mp_canvas_drawer`
```
<img :src="shareImage" class="share-image" />
<canvasdrawer :painting="painting" class="canvasdrawer" @getImage="eventGetImage"/>
```


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
