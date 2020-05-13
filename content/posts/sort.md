---
title: "四种排序算法"
date: 2020-03-18T22:14:46+08:00
draft: false
---

# 四种排序算法

1. 选择排序

```
//循环里第i个数字与最小数字交换顺序
let swap = (array, i, j) => {
    let temp = array[i]
    array[i] = array[j]
    array[j] = temp
}
//找到数组最小数字的索引，index一直标记着
let minIndex = (numbers) => {
    let index = 0
    for(let i=1; i<numbers.length; i++){
        if(numbers[i] < numbers[index]){
            index = i
        }
    }
    return index
}

let sort = (numbers) => {
    for(let i=0; i< numbers.length -1; i++){
        console.log(numbers,i,numbers.slice(i),)
        let index = minIndex(numbers.slice(i))+ i
        if(index!==i){
          swap(numbers, index, i)
        }
    }
    return numbers
}
console.log(sort([12,33,4,7,9,30,66]))

```

2. 快速排序

```
let quickSort = arr => {
    if (arr.length <= 1) { return arr; }
    let pivotIndex = Math.floor(arr.length / 2);
    let pivot = arr.splice(pivotIndex, 1)[0];
    let left = [];
    let right = [];
    for (let i = 0; i < arr.length; i++){
        if (arr[i] < pivot) {
            left.push(arr[i])
        } else {
            right.push(arr[i])
        }
    }
    return quickSort(left).concat(
    [pivot], quickSort(right) )
}
```

3. 归并排序

```
let mergeSort = arr =>{
    let k = arr.length
    if(k===1){return arr}
    let left = arr.slice(0, Math.floor(k/2))
    let right = arr.slice(Math.floor(k/2))
    return merge(mergeSort(left), mergeSort(right))
}
let merge = (a, b)=>{
    if(a.length === 0) return b
    if(b.length === 0) return a
    return a[0] > b[0] ?
    [b[0]].concat(merge(a, b.slice(1))) :
    [a[0]].concat(merge(a.slice(1), b))
}
```

4. 计数排序

```
let countSort = arr =>{
    let hashTable = {}, max = 0, result = []
    //遍历数组
    for(let i=0; i<arr.length; i++){
        if(!(arr[i] in hashTable)){
            hashTable[arr[i]] = 1
        }else{
            hashTable[arr[i]] += 1
        }
        if(arr[i] > max) {max = arr[i]}
    }
    //遍历哈希表
    for(let j=0; j<=max; j++){ //
        if(j in hashTable){
            for(let i = 0; i<hashTable[j]; i++){
                result.push(j)
            }
        }
    }
    return result
}

```
