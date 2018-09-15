# vue-oa

> A Vue.js project  

- 项目概述
  - 该项目是一套OA系统，主要运行在PC端
  - 技术栈：vue + vue-router

- 项目开发流程
  - 首先规划项目的组成部分，也就是组件
    - 头部组件
    - 侧边栏组件
      - 这里主要是承担路由跳转的任务
      - 二级子菜单、子路由
    - 其余部分视图由路由切换来控制

- 项目过程遇到的问题
  - 侧边栏菜单组件的开发
    - 如何让侧边栏独自撑起整个页面？
    - 点击二级菜单不要触发一级菜单事件？
      - 二级菜单添加@click.stop，阻止事件冒泡
    - 关于菜单hover时的样式


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