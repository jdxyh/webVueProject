# vuetest

> this is my vuetest

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

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# 项目说明文档

# 一：项目实现的需求：
1 模仿'去哪儿'界面，实现简单的功能浏览操作<br />
# 二：运行环境搭建
1 下载 node.js 项目管理工具,使之能运行npm包管理工具<br />
2 选用git仓库托管平台,github 码云等,操作简单的git命令<br />
3 下载Vue脚手架工具（详细参看Vue官方说明文档）<br />
npm install --global vue-cli<br />
vue init webpack my-project<br />
cd my-project<br />
npm install<br />
npm run dev(npm run start)<br />
4 查阅Vue目录结构，查看目录结构下各文件的作用<br />
# 三：项目Coding开始
1 对项目中的index.html<mete></meta>配置进行优化。
<meta name="viewport" content="width=device-width,initial-scale=1.0,
    	minimum-scale=1.0,maximum-scale=1.0,user-scalable=no">
2 引入 reset.css和border.css文件，统一初始化样式，1像素边框问题<br />
在main.js中导入<br />
import '@/assets/styles/reset.css'<br />
import '@/assets/styles/border.css'<br />
3 引入fastclick库文件，决绝300毫秒延时:
npm install fastclick --save<br />
在main.js中导入<br />
import fastClick from 'fasterclick'
fastClick.attach(document.body)
4 引入iconfont图标，进入网站iconfont进行项目管理<br />
选择图标，加入购物车，打包下载
# 四：首页Header.vue区域开发
1 使用 stylus 样式开发 <br />
npm install stylus --save<br />
npm install stylus-loader --save<br />
2 拆分Home.vue大组件为多个小组件，创建Header.vue组件<br /><br />
在Home.vue大组件中导入Header.vue<br />
import HomeHeader from './components/Header'<br />
在Home.vue组件声明中添加Header.vue<br />
3 再样式中应用 stylus<br />
<style lang = "stylus" scoped><br />
</style><br />
# 五：iconfont的使用和代码优化<br />
1 进入iconfont中搜索要的图标，放入购物车，打包下载<br />
在<template><template>中添加使用<br />
<span class  = "iconfont">添加引入代码（如）&#xe624</span><br />
2 抽取通用颜色，添加到自定义varibles.styl文件<br />
导入（样式中引入其他样式，需要@）<br />
@import '@assets/stylus/varibles.styl'<br />
3 在全局配置build/webpack.base.conf.js中配置自定义快捷导入<br />
# 六：首页轮播Swiper.vue图开发
1 git 创建分支，以便企业中的代码回滚，分类整合等。git分支相关命令<br />
2 借助第三方的轮播插件，实现图片轮播效果图
进入git 搜索 vue-awesome-swiper,查看相关的帮助文档导入项目中
npm install vue-awesome-swiper@2.6.7 --save
3 实现轮播效果，在引入第三发插件后，标签<swiper></swiper>中添加一个图片标签，
在<script></script>中取得图片所在块的标签，作列表循环，实现轮播效果。















