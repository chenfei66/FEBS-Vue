### FEBS-Vue
![https://img.shields.io/badge/build-success-brightgreen.svg?longCache=true&style=flat-square](https://img.shields.io/badge/build-success-brightgreen.svg?longCache=true&style=flat-square)
![https://img.shields.io/badge/license-MIT-blue.svg?longCache=true&style=flat-square](https://img.shields.io/badge/license-MIT-blue.svg?longCache=true&style=flat-square)
![https://img.shields.io/badge/springboot-2.1.0-yellow.svg?longCache=true&style=flat-square](https://img.shields.io/badge/springboot-2.1.0-yellow.svg?longCache=true&style=flat-square)
![https://img.shields.io/badge/shiro-1.4.0-orange.svg?longCache=true&style=flat-square](https://img.shields.io/badge/shiro-1.4.0-orange.svg?longCache=true&style=flat-square)
![https://img.shields.io/badge/vue-2.5.17-brightgreen.svg?longCache=true&style=flat-square](https://img.shields.io/badge/vue-2.5.17-brightgreen.svg?longCache=true&style=flat-square)

FEBS-Vue为[FEBS-Shiro](https://github.com/wuyouzhuguli/FEBS-Shiro)的前后端分离版本，前端使用Vue全家桶，组件库采用[Ant-Design-Vue](https://vuecomponent.github.io/ant-design-vue/docs/vue/introduce-cn/)

### 预览地址

服务器带宽小，初次加载较慢，请耐心等待：[http://111.230.157.133:8081](http://111.230.157.133:8081)。

账号密码：

账号 | 密码| 权限
---|---|---
scott | 1234qwer | 注册账号，拥有查看，新增导出等权限，但不能新增用户
jack | 1234qwer |普通账户，仅拥有所有页面查看权限
mrbird | 进群获取，或者自己搭建体验 |超级管理员，拥有所有增删改查权限

### 功能模块
```
├─系统管理
│  ├─用户管理
│  ├─角色管理
│  ├─菜单管理
│  ├─部门管理
│  └─字典管理
├─系统监控
│  ├─在线用户
│  ├─系统日志
│  ├─Redis监控
│  ├─请求追踪
│  └─系统信息
│     ├─JVM信息
│     ├─服务器信息
│     └─Tomcat信息
│─任务调度
│  ├─定时任务
│  └─调度日志
│─网络资源
│  ├─天气查询
│  ├─影视资讯
│  │  ├─即将上映
│  │  └─正在热映
│  └─每日一文
└─其他模块
   └─导入导出

```
### 技术选型

#### 前端
- [Vue 2.5.17](https://cn.vuejs.org/),[Vuex](https://vuex.vuejs.org/zh/),[Vue Router](https://router.vuejs.org/zh/)
- [Axios](https://github.com/axios/axios)
- [vue-apexcharts](https://apexcharts.com/vue-chart-demos/line-charts/)
- [ant-design-vue](https://vuecomponent.github.io/ant-design-vue/docs/vue/introduce-cn/)
- [webpack](https://www.webpackjs.com/),[yarn](https://yarnpkg.com/zh-Hans/)

#### 后端
- [Spring Boot 2.1.0](http://spring.io/projects/spring-boot/)
- [Mybatis](http://www.mybatis.org/mybatis-3/zh/index.html),[TK Mapper](https://gitee.com/free/Mapper/wikis/Home),[Pagehelper](https://gitee.com/free/Mybatis_PageHelper)
- [MySQL 5.7](https://dev.mysql.com/downloads/mysql/5.7.html#downloads),[Hikari](https://brettwooldridge.github.io/HikariCP/),[Redis](https://redis.io/)
- [Shiro](http://shiro.apache.org/),[JWT](https://jwt.io/)

### 系统特点

1. 根据不同用户权限动态构建路由
2. RESTFul风格接口
3. 前后端请求参数校验
4. 支持Excel导入导出
5. 前端页面布局多样化，主题多样化
5. 自定义Vue权限指令来控制DOM元素渲染与否：

指令 | 含义| 示例
---|---|---
v-hasPermission | 当用户拥有列出的权限的时候，渲染该元素 |`<template v-hasPermission="'user:add','user:update'"><span>hello</span></template>`
v-hasAnyPermission | 当用户拥有列出的任意一项权限的时候，渲染该元素 |`<template v-hasAnyPermission="'user:add','user:update'"><span>hello</span></template>`
v-hasRole | 当用户拥有列出的角色的时候，渲染该元素 |`<template v-hasRole="'admin','register'"><span>hello</span></template>`
v-hasAnyRole | 当用户拥有列出的任意一个角色的时候，渲染该元素 |`<template v-hasAnyRole="'admin','register'"><span>hello</span></template>`

### 请求流程
下图展示了在FEBS-Vue中一个请求的完整流程：

![request.png](images/request.png)
### 系统预览
![1.png](images/1.png)

![2.png](images/2.png)

![3.png](images/3.png)

![4.png](images/4.png)

![6.png](images/6.png)

![7.png](images/7.png)

![8.png](images/8.png)

![9.png](images/9.png)

![10.png](images/10.png)

### 使用教程

#### 后端

1. IDEA 或者 Eclipse安装lombok插件

2. 新建MySQL（版本5.7.x）数据库，导入[SQL](https://github.com/wuyouzhuguli/FEBS-Vue/blob/master/sql/febs.sql)文件

3. 导入项目

4. 修改数据库配置，redis配置，等待Maven下载依赖

5. 启动项目

#### 前端

切换到front文件夹下
```
# 安装yarn
npm install -g yarn

# 下载依赖
yarn install

# 启动
yarn start

# 编译
yarn build
```

> 详细文档编写中...
### 鸣谢

感谢以下优秀的开源项目：

- [ant-design-vue](https://github.com/vueComponent/ant-design-vue)

- [vue-antd-admin](https://github.com/iczer/vue-antd-admin)

- [ExcelKit](https://gitee.com/wuwenze/ExcelKit)

### 反馈交流
![QQ](images/QQ.jpg)