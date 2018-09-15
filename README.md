# vue-oa

> A Vue.js project  

- 项目概述
  - 该项目是一套OA系统
  - 技术栈：vue + vue-router

- 项目开发流程
  - 首先规划项目的组成部分，也就是组件
    - 头部组件
    - 侧边栏组件
      - 这里主要是承担路由跳转的任务
      - 二级子菜单、子路由
    - 其余部分视图由路由切换来控制


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