---
title: "重名了改一下"
date: 2022-03-02T23:34:24+08:00
---

### Variable elevation; Event bubble; Prototype
#### 变量提升
预解析；变量提升到最上面，值不变；只有有作用域的位置才会发生变量提升。  
JS的变量具有唯一性，变量提升的变量会覆盖掉前面的定义值。  
函数的变量提升优先级次于变量。函数变量提升的值可以提升。
#### 事件冒泡

子级元素会继承父级元素的事件。  
  `event.cancelBubble=true;` 阻止事件冒泡,防止父级的事件到子级中。

#### 原型
原型链给原型加方法。  
原型可以用json的方法去赋予。
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>
  <script type="text/javascript">
    Array.prototype.zs=function(){
      alert(this);
    };
    [1,2,3].zs();

    Function.prototype.zs=function(){
      alert("dont speak now");
    };
    function a(){};
    a.zs();

  </script>
</body>
</html>

```
##### 继承原型
`a.prototype=b.prototype`
more definited you can set `a.prototype.nn=b.prototype.nn`  
`new a().nn()`

##### json的方法赋值
```
a.prototype={
  'mm':function(){
    alert(this.a+this.b);
  },
  'nn':function(){
    alert(2);
  }
}
```
### AJAX(AHR)
get   
post   
同步  
异步  
后台语言： php .net java nodeJS  
服务器的状态码：2成功；3重定向；4失败   
状态码：怎么把responseText弄出来  
**ajax readyState**
```
0 - (未初始化)还没有调用send()方法
1 - (载入)已调用send()方法，正在发送请求
2 - (载入完成)send()方法执行完成，
3 - (交互)正在解析响应内容
4 - (完成)响应内容解析完成，可以在客户端调用了
```
```
ajax.onreadystatechange=function(){
  if(ajax.readyState==4){
    console.log(ajax.responseText)
    console.log(ajax.status)
  }
  // console.log('ajax.readyState');
}
```

nodeJS优点：
1. nodeJS 比 php快86倍
2. VUE和REACT都基于nodeJS
3. 基于cmd，编译型语言非内置

#### 第一个nodejs脚本
```
var http= require('http');
http.createServer(function(request,response){
  console.log(request.url);
}).listen(9217);
// 返回监听的9217端口的url
```
```
var http= require('http');
http.createServer(function(request,response){
  // console.log(request.url);
  response.setHeader('Access-Control-Allow-Origin','*')
  <!-- 实现跨域 -->
  console.log('sb coming');
  // 只要有请求来控制台就会输出提示
  response.write('Im LauYing');
  response.end();
}).listen(9217);
```

#### 前端脚本
```
var ajax= new XMLHttpRequest();
ajax.open('get','http://localhost:9217/',false);
// 新建一个和后台服务器交换数据的对象，打开一个本地的端口，同步干完一条命令才下一条，异步分开干。
ajax.send();
console.log(ajax.responseText)
```
