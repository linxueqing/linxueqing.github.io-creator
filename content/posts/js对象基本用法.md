---
title: "Js对象基本用法"
date: 2020-03-07T18:50:47+08:00
draft: false
---

# Js 对象基本用法

## 1：声明对象的两种语法

```
let obj1 = new Object({'name':'Jerry'});   //标准写法
let obj2={'name':'Tom'};    //常用写法

```

## 2：如何删除对象的属性

```
let obj={'name':'Tom','age':18};
delete obj['name'];    //删除name属性
```

## 3：如何查看对象的属性

```
let obj={'name':'Tom'};
Object.keys(obj);  //查看对象属性
Object.values(obj);  //查看对象值
Object.entries(obj);  //查看对象
console.dir(obj);   //查看对象
```

只查看属性

```
let obj={'name':'Tom'};
obj['name'];
obj.name
```

## 4：如何修改或增加对象的属性

属性存在就是在修改，不存在就是在增加

```
let obj={'name':'Tom'};
obj['name'] = 'Jack';
Object.assign(obj,{p:1,p1:2});
let common = {'国籍','中国'};
let person = Object.create(common);
```

## 5：'name' in obj 和 obj.hasOwnProperty('name') 的区别

- 'name' in obj 判断`obj`对象是否存在`name`属性
- obj.hasOwnProperty('name')判断`name`是不是自有属性
