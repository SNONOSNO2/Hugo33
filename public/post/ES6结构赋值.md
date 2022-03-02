### 块级作用域
解决密封空间的问题
```
<input value="1" type='button'>
<input value="2" type="button">
<input value="3" type="button">
<script type="text/javascript">
  let allInput=document.getElementsByTagName('input');
  // for(var i=0;i<allInput.length;i++){
  //   // allInput[i].onclick=function(){
  //   //   alert(i)
  //   //   // 赋予对象点击事件，点击的瞬间i已循环完毕，返回值都是3
  //   (function(x){
  //     console.log(x)
  //   })(i)
  //   //匿名函数，函数的参数直接传递,相当于同时生成3个匿名函数
  //   }
  //
  for(let i=0;i<allInput.length;i++){
    allInput[i].onclick=function(){
      console.log(i);
    }
  }
</script>
```
### 结构赋值
json需要使用键值赋值
```
let [a,b,c,d]=jason;
console.log(a,b,c,d)
```

### Bind
任何函数都可以用call调用自己，第一个参数是this，第二个参数是形参,不会调用自己，使用需要（）。
