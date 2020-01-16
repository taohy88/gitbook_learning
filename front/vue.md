# Vue

[TOC]

---



## Vue源码剖析之整体流程

参考资料：[Vue源码剖析之整体流程]([http://deal.kaikeba.com/link/e4512aea-6d4a-4017-8ef3-3f81b8e12046?share_token=Ao4i2TdC&utm_source=%E8%B5%84%E6%96%99%E9%93%BE%E6%8E%A5%E5%85%A5%E5%BA%93&utm_medium=%E5%BE%AE%E4%BF%A1&utm_content=Vue%E6%BA%90%E7%A0%81%E5%89%96%E6%9E%90%E4%B9%8B%E6%95%B4%E4%BD%93%E6%B5%81%E7%A8%8B](http://deal.kaikeba.com/link/e4512aea-6d4a-4017-8ef3-3f81b8e12046?share_token=Ao4i2TdC&utm_source=资料链接入库&utm_medium=微信&utm_content=Vue源码剖析之整体流程))

----

##### Vue 源码调试环境搭建

1. 获取Vue

2. 源码查看版本号：package.json--version

3. 文件结构

   dist：输出

   examples：实例

   flow：类型声明

   packages：scripts：打包脚本

   src：源码目录 

   compiler编译器 

   core核心 

   platforms平台 

   server服务端 

   types：TS类型说明

4. 调试环境搭建

   VSCode

   安装依赖 ：npm install

   安装rollup：npm install rollup -g

   修改dev脚本：package.json-scripts-dev-"dev": "rollup -w -c scripts/config.js --sourcemap --environment TARGET:web-full-dev"

   打包：npm run dev

5. 

   

##### 探寻入口文件

1. xamples文件夹创建测试文件，引入vue.js
2. src\platforms\web\entry-runtime-with-compiler.js



##### Vue初始化流程分析

扩展了$mount 方法：处理template和el选项，尝试编译他们为render函数

src\platforms\web\runtime\index.js定义$mount方法，执行挂载mountComponent(this, el, hydrating)实现了path方法



src\core\index.js定义全局API 

```
initGlobalAPI(Vue)

Vue.set = set
Vue.delete = del
Vue.nextTick = nextTick
initUse(Vue)
initMixin(Vue)
initExtend(Vue)
initAssetRegisters(Vue)
```

src\core\instance\index.js

```
function Vue (options) {
  if (process.env.NODE_ENV !== 'production' &&
    !(this instanceof Vue)
  ) {
    warn('Vue is a constructor and should be called with the `new` keyword')
  }
  this._init(options)
}

initMixin(Vue)
stateMixin(Vue)
eventsMixin(Vue)
lifecycleMixin(Vue)
renderMixin(Vue)
```

init Vue

src\core\instance\init.js

```
// expose real self
    vm._self = vm
    initLifecycle(vm)
    initEvents(vm)
    initRender(vm)
    callHook(vm, 'beforeCreate')
    initInjections(vm) // resolve injections before data/props
    initState(vm)
    initProvide(vm) // resolve provide after data/props
    callHook(vm, 'created')
```



##### Vue源码学习整体流程总接



##### 数据响应化流程分析



##### 数据响应化原理







## 一步到位VUE精讲

参考资料：[一步到位VUE精讲]([http://deal.kaikeba.com/link/96f2f02d-8ac0-40fa-bdb7-ce365ad7a9a3?share_token=Ao4i2TdC&utm_source=%E8%B5%84%E6%96%99%E9%93%BE%E6%8E%A5%E5%85%A5%E5%BA%93&utm_medium=%E5%BE%AE%E4%BF%A1&utm_content=%E4%B8%80%E6%AD%A5%E5%88%B0%E4%BD%8DVUE%E7%B2%BE%E8%AE%B2](http://deal.kaikeba.com/link/96f2f02d-8ac0-40fa-bdb7-ce365ad7a9a3?share_token=Ao4i2TdC&utm_source=资料链接入库&utm_medium=微信&utm_content=一步到位VUE精讲))

---





