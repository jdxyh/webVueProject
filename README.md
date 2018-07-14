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
 

	

