### ECMA Script 6+ and new feature
#### 声明方式  
- let/const  
php java 变量  
常量可以复制

#### 字符串
- String.fromCharCode(编码);  
charCodeAt() 获取编码
- a.repeat(3) 重复3次
- includes (similar to indexof)
```
let a='fdsdfs'
console.log(a.includes('s',1));
返回查找的布尔值,从第几位开始
```
- startsWith()
返回开头查找的目标值的布尔值，从第几位开始
- endsWith()
返回从第几位结束的目标值的布尔值，从第几位结束

#### 模板
${}
```
let json={
  'div':`<div></div>`
  'span':`<span></span>`
}
document.write(`${json.div+json.span+json.div}`);
```

#### 数组方法
find
- 第一个参数  
- 第二个参数
- 第三个参数

#### 函数
##### 箭头函数     
x(函数名)=x（变量）=>x（返回值）   
##### 延展参数   
没有传参的情况下使用延展的参数，延展参数可以延展任何参数。
```
function show(x=5){
  console.log(x)
};
show();
```
##### 扩展运算符
函数中的参数用`...X`代表对应选择的数组元素；
在数组中可以合并数组。
#### 简易选项卡
jason{}可以有set、get方法，赋值执行set函数，不赋值执行get函数
#### 生成器函数
function* 函数名()   
函数名.next();
##### yield
yield 可以实现无限的next()
