---
title: "Vue 中的 .sync 修饰符有什么用"
date: 2020-05-31T17:51:03+08:00
draft: false
---

# Vue 中的 .sync 修饰符有什么用

- vue 的.sync 修饰符的功能是：当一个子组件改变了一个 prop 的值时，这个变化也会同步到父组件中所绑定。
- .sync 修饰符其实就是一个语法糖

## 举个例子

- 子组件代码

```
  <!-- Child.vue -->
  <template>
  <div id="child">
    <div class="change" v-if="show"></div>
    <button class="btn" @click="$emit('update:show', !show)">点我试试</button>
  </div>
  </template>
<script>
export default {
  name: "Child",
  props: ["show"]
};
</script>

```

- 父组件

```
<template>
  <div id="app">
    <Child :show.sync="valueChild"/> <!-- A处 -->
    <Child :show="valueChild" @update:show="valueChild = $event"></Child> <!-- B处 -->
  </div>
</template>

<script>
import Child from "./Child";

export default {
  name: "App",
  components: { Child },
  data() {
    return {
      valueChild: true
    };
  }
};
</script>

```
