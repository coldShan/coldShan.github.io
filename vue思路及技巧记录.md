# vue 思路及技巧记录

[toc]

## 全局组件的使用

## 全局过滤器的使用

## `mixin`的使用

## `Router`中钩子函数的使用，如：`beforeEach`

## `Vuex`

- ### `action`可执行异步方法

## `axios`

- ### 兼容性处理

```
npm install --save babel-polyfill
// 步骤2 在 vue.config.js 文件中加入以下内容
module.exports = {
  configureWebpack: config => {
      return {
          entry: {
              app:['babel-polyfill', './src/main.js']
          }
      }
  }
}
```

## 子组件获取未在`props`中声明的属性

> 使用 `this.$attrs`

```
// 父组件
<home title="这是标题" width="80" height="80" imgUrl="imgUrl"/>

// 子组件
mounted() {
  console.log(this.$attrs) //{title: "这是标题", width: "80", height: "80", imgUrl: "imgUrl"}
}
```

*若属性已经在`props`中声明过，则无法通过`$attrs`获取到*
