---
title: "面对对象"
date: 2022-03-02T23:34:24+08:00
---
 
#### 类
window-string-substring/indexof(方法)    
-number-tostring

[1,2,3].constructor 精准告诉你什么类
Array.prototype 告诉你类的原型
Object.prototype.a=10 所有的类都等于10
Object.prototype.toString.call([1,2,3]) 返回查询对应的类

Array.prototype.split=function(){} 给原型类添加方法后下面代码才能正常运行
var a=['afd'];
console.log(a.spilt(''))

String.prototype.split.call(a) 这个能返回a自己，可以使用所有的方法

```
ES6
class a{
  contructor(){
写类的方法
    this.x=10;
    console.log(this.x)
  }
};
new a();
```
#### 原型
#### 原型链
`_proto_`

#### 面向对象继承

继承 extends super
```
class show(){
  constructor(l){
    this.x=l;
  }
  定义一个show的class并指定方法，让x赋值为1，自由属性
  m(){
    alert(this.x);
  }
  类中定义的方法
}
new show(1).m();

如何继承show
class me extends show{
  constructor(l){
    super(l)
  }
}
class继承方法，super继承this
new me(1).m();
```
