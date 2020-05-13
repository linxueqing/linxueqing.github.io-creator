---
title: "jQuery 的常用功能"
date: 2020-03-23T22:56:15+08:00
draft: false
---

# jQuery 的常用功能

1. jQuery 如何获取元素

```
　//选择表达式可以是CSS选择器：
  $(document) //选择整个文档对象
　$('#myId') //选择ID为myId的网页元素
　$('div.myClass') // 选择class为myClass的div元素
　$('input[name=first]') // 选择name属性等于first的input元素

  //也可以是jQuery特有的表达式：
  $('a:first') //选择网页中第一个a元素
　$('tr:odd') //选择表格的奇数行
　$('#myForm :input') // 选择表单中的input元素
　$('div:visible') //选择可见的div元素
　$('div:gt(2)') // 选择所有的div元素，除了前三个
　$('div:animated') // 选择当前处于动画状态的div元素
```

2. jQuery 的链式操作是怎样的

就是最终选中网页元素以后，可以对它进行一系列操作，并且所有操作可以连接在一起，以链条的形式写出来

```
$('div').find('h3').eq(2).html('Hello');
```

分解开来：

```
$('div')   //找到div元素
　.find('h3')   //选择其中的h3元素
　.eq(2)   //选择第3个h3元素
　.html('Hello');   //将它的内容改为Hello
```

3. jQuery 如何创建元素

   创建新元素的方法非常简单，只要把新元素直接传入 jQuery 的构造函数就行

```
$('<p>Hello</p>');
$('<li class="new">new list item</li>');
$('ul').append('<li>list item</li>');
```

4. jQuery 如何移动元素

第一种方法是使用.insertAfter()，把 div 元素移动 p 元素后面：

```
$('div').insertAfter($('p'));
```

第二种方法是使用.after()，把 p 元素加到 div 元素前面：

```
$('p').after($('div'));
```

5. jQuery 如何修改元素的属性

```
.attr() 取出或设置某个属性的值
```
