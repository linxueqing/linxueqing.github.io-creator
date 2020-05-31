---
title: "说说对 Vue 数据响应式的理解"
date: 2020-05-18T22:37:41+08:00
draft: false
---

# 说说对 Vue 数据响应式的理解

```
const vm =new Vue({data:{n:0}})
```

1.  data 会被 Vue 监听，被篡改，本来的 n 会变成 get n ,set n
2.  vm 是对 Vue 的代理，每次对 data 的读写都会被 Vue 监控，不论是读写 data 本身，还是读写 data 的代理
3.  Vue 会在 data 变化的时候更新 UI
