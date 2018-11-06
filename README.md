# vue-miniueditor
安装
```
npm install vue-miniueditor --save
```
打包生产环境
```
npm run build
```
基于 百度UMEditor 的 VUE 版本， 原作是[JakeLaoyu](https://github.com/JakeLaoyu)
在基础上增加了 convertImageToBase64Enable config的参数，支持剪贴板文件或者拖拽图片到编辑器以base64位生成srcData的img图片

需要在config中配置,不需要服务器后台支持可以预览效果
```
config:{
  convertImageToBase64Enable:true
}
```
-----------------------------------------------------@1.0.8
新增插件 base64Image，可直接在config toolbar里面配置，可以直接将本地图片转为base64位编码并插入编辑器中


![效果预览](https://github.com/Xekin-FE/vue-miniumeditor/blob/master/src/assets/ReadMe.png)

使用方法

### 全局注册 使用 main.js 引入
```
import vUeditor from 'vue-miniueditor'
Vue.use(vUeditor)
```
在项目中
```
<template>
  <v-ueditor :config="config" @ready="ready"></v-ueditor>
</template>
<script>
  export default{
    data(){
      return{
        ue:'',
        config:{
          convertImageToBase64Enable:true,
          newStyle:true
        } //具体配置参考官方文档
      }
    },
    methods:{
      ready(ue){
        this.ue = ue
      }
    }
  }
</script>
```

### 项目引入
```
<template>
  <v-ueditor :config="config" @ready="ready"></v-ueditor>
</template>
<script>
  import vUeditor from 'vue-miniueditor'
  export default{
    components:{ vUeditor },
    data(){
      return{
        ue:'',
        config:{
          convertImageToBase64Enable:true,
          newStyle:true
        } //具体配置参考官方文档
      }
    },
    methods:{
      ready(ue){
        this.ue = ue
      }
    }
  }
</script>
```
