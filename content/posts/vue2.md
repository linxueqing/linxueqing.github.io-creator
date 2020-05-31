---
title: "Vue中computed和watch的区别"
date: 2020-05-20T22:13:58+08:00
draft: false
---

# Vue 中 computed 和 watch 的区别

1. computed 是计算属性，watch 是监听
2. computed 的值不需要加括号，可以直接当属性用
3. computed 的计算结果会自动缓存
4. watch 有一个选项 immediate 在最初绑定的时候就执行
5. watch 还有一个选项 deep 代表是否深度监听
