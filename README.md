# vue-miniueditor
```
npm install vue-miniumeditor --save
```

基于 百度UMEditor 的 VUE 版本， 原作是[JakeLaoyu](https://github.com/JakeLaoyu)
在基础上增加了 convertImageToBase64Enable config的参数，支持剪贴板文件或者拖拽图片到编辑器以base64位生成srcData的img图片

需要在config中配置,不需要服务器后台支持可以预览效果
```
config:{
  convertImageToBase64Enable:true
}
```

![效果预览](https://github.com/Xekin-FE/vue-miniumeditor/blob/master/src/assets/ReadMe.png)
