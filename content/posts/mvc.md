---
title: "MVC总结"
date: 2020-05-06T21:36:54+08:00
draft: false
---

# MVC 总结

1. MVC 三个对象分别做什么

   M-Model（数据模型）数据以及对数据的增删查改

   ```
   const m = {
       data:{
           n:0
       },
       create(){},
       delete(){},
       update(data){},
       get(){}
   }
   ```

   V-View（视图模型）负责所有的 UI 界面

   ```
   const v={
       el:null,
       html:`
       <div></div>
       `,
       init(container){
           v.el=container
       },
       render(n){
           if(v.el.children.length!==0)v.el.empty()
           $(v.html.replace('{{n}}',n)).appendTo(v.el)
       }
   }
   ```

   C-Controller（控制器）负责其他

   ```
   const c={
       init(){

       },
        events:{
            'click #add1':'add'
        },
        add(){
            m.update(data:{ n:m.data.n+1})
        }
   }

   ```

2. EventBus 有哪些 API，是做什么用的，给出伪代码示例

```
    import $ from 'jquery'
    class EventBus{
        constructor(){
            this._eventBus=$(window)
        }
        on(eventName,fn){
            return this._eventBus.on(eventName,fn)
        }
        trigger(eventName,data){
            return this._eventBus.trigger(eventName,data)
        }
        off(eventName,fn){
            return this._eventBus.off(eventName,fn)
        }
    }
    export default EventBus
```

3. 表驱动编程是做什么的

   当我们看到大批相似但不重复的代码，我们可以利用表这一数据结构，
   抽取出代码中的核心数据，重构相似的代码。这样不仅可以减少重复代码，
   还可以提高代码的可读性、可扩展性等。

4. 我是如何理解模块化的

   模块化是指将一个复杂的程序依据一定的规则(规范)封装成几个块(文件), 并组合在一起。
   块的内部数据与实现是私有的, 只是向外部暴露一些接口(方法)，用于与外部其它模块通信。
   模块化是一种分治的思想体现，各个模块分而治之，各司其职。

   模块化开发好处：

- 避免命名冲突(减少命名空间污染)
- 更好的分离/管理
- 高复用性
- 高可维护性
