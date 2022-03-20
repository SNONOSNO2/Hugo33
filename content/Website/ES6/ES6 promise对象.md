---
title: "Promise对象"
date: 2022-03-02T23:34:24+08:00
---



### Promise
promise是个对象   
只要触发就完成了任务结束生命周期。
可以无限回调
```
new Promise(function(Resolved,Reject){
  Resolved();
}).then(function(){
  alert('成功')
  },function(){
    alert('失败')
    })

function showPromise(res){
  return new Promise((resolve,reject)=>{
    resolved(res)
    }).then ((x)=>{console.log(x)},()=>{

      })
}
showPromise('yours');
```
实现点击显示循环
```
let index=0;
ipt.onclick=x=>{
  index++;
  new Promise((succ,error)=>{
    index%2==1?succ();error();
    }).then(()=>{
        div1.style.display='none';
      },()=>{
        div1.style.display='block';
        })
};
```
then(成功函数).catch(失败函数)
#### throw
抛出异常
#### race
竞速方法
只看第一个执行完成的promise
#### all
要不然就是全胜要么全部失败，全部成功就全部输出
### Webwork
