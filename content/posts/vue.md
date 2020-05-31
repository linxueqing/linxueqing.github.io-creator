---
title: "浅析 Vue 两个版本的区别和使用方法"
date: 2020-05-14T21:32:17+08:00
draft: false
---

# 浅析 Vue 两个版本的区别和使用方法

1. 两个版本对应的文件名

   分别是 Vue 完整版（vue.js）和 Vue（vue.runtime.js ）非完整版

2. template 和 render 怎么用

   render 不需要编译器

   ```
   new Vue({
       render(h){
           return h('div',this.hi)
       }
   })

   ```

   template 需要编译器

   ```
   new Vue({
       template:'<div>{{hi}</div>'
   })
   ```

3. 如何用 codesandbox.io 写 Vue 代码
   - 进入 codesandbox.io，不要登陆
   - 点击 create sandbox 按钮，选择 vue 模板
   - 可以直接修改保存
   - 也可也 File-Export to Zip 导出你的 Vue 项目
