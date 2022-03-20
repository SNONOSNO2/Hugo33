---
title: "字符串模版"
date: 2022-03-02T23:34:24+08:00
---
### 字符串模板
#### 字符串可以放入参数，传参
```
function show(n){
  var json=(
    f:20,k:30
    )
  return json;
};
var string ='show the return is ${show().f}'
console.log(string)
```
数组的map
```
map 用法和find/findIndex一样，会返回大数组
```
#### 标签模板
#### 模板字符串嵌套
```
createNode=json=>`<div class=outNode>
  ${json.topValue.map((v)=>
    `<input type=button value=${v}>`).join('')}
  ${json.bottommInner.map((v)=>
    `<div>${v}</div>`).join('')}
  </div>

document.body.innerHTML=createNode(jsonData)    
`
```
#### 字符串的string.raw()方法
转义直接输出`\\n`
### number篇
#### 二进制
0b后加二进制，反写
#### 特殊运算 位运算/次方运算
3<<2  //3* 2 *2
### 方法篇
#### SET()
```
var set=new Set();
set.add(1);
set.add(2);
console.log(Set.prototype)
console.log(set.has(5))


const $=>obj=>[...document.querySelector(obj)];
var allDiv= new Set($('.outNode>div'));
//找到所有outNode下的div
console.log(allDiv)
```

#### MAP()
```
var mapNode= new Map();
mapNode.set('a','thin');
mapNode.set('b','fat');
mapNode.set('c','rich');
console.log(mapNode.get('c'))

for(let [k,v] of mapNode){
  console.log(k,v)
}
```
