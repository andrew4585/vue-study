## vuex是什么

Vuex 是一个专为 Vue.js 应用程序开发的**状态管理模式**

### 什么是“状态管理模式”？

``` javascript
new Vue({
  // state
  data () {
    return {
      count: 0
    }
  },
  // view
  template: `
    <div>{{ count }}</div>
  `,
  // actions
  methods: {
    increment () {
      this.count++
    }
  }
})
```

这个状态自管理应用包含以下几个部分：

* **state**，驱动应用的数据源；
* **view**，以声明方式将state映射到视图；
* **actions**，响应在view上的用户输入导致的状态变化。

以下是一个表示“单向数据流”理念的极简示意：
<img src='images/flow.png' style='width:60%'/>

### 解决问题
当我们的应用遇到多个**组件共享状态**时：

* 多个视图依赖于同一状态。
* 来自不同视图的行为需要变更同一状态。
