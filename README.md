# 属性
- 自定义属性 props
`组件props中声明的属性`
- 原生属性 attrs
`没有声明的属性，默认自动挂载到组件根元素上, 设置inheritAttrs 为 false 可以关闭自动挂载`
- 特殊属性 class style
`挂载到组件根元素上, 支持字符串、对象、数组等多种语法`

---

# 事件
- 普通事件
`@click, @input, @change, @xxx等事件通过this.$emit('xxx', ....)触发`
- 修饰符事件
`@input.trim, @click.stop, @submit.prevent等, 一般用于原生HTML元素, 自定义组件需要自行开发支持`

---

# 插槽
- 普通插槽
```
<template slot="xxx">...</template>
推荐：<template v-slot:xxx>...</template>
```
- 作用域插槽
```
<template slot="xxx" slot-scope="props">...</template>
推荐：<template v-slot:xxx="props">...</template>
```
 ---

 # 大属性
 - 属性
    1. 自定义属性 props
    2. 原生属性 attrs
    3. 特殊属性 class、style
 - 事件
    1. 普通事件
    2. 修饰符事件
 - 插槽
    1. 普通插槽
    2. 作用域插槽

---

# 双向绑定 or 单向数据流
- Vue是单向数据流，并不是双向绑定
- Vue的双向绑定不过是语法糖
- Object.defineProperty是用来做响应式更新的，和双向绑定没关系

---

