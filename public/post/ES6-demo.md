### ES6版选项卡
### ES6 AJAX
```
function ajax(url){
  return new Promise((succ,error)=>{
    var ajax= new XMLHttpRequest();
    ajax.open('get',url,true);
    ajax.send;
    ajax.onload=function(){
      succ(ajsx.responseText);
    };
    ajax.onerror=function(){
      error();
    };
    }).then((text)=>{
      cosole.log(text);
      }).catch(()=>{
        console.log(1);
        })
}
```
