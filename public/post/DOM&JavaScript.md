## DOM and JavaScript

### DOM
DOM= Document Object Model  
You can regard it as html label which can be manipulated by JavaScript.

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>html tag</title>
  <style type="text/css">
  #mydiv{width: 100px;height: 100px;background: black}
  </style>
  <script>
    window.onload= function(){
      // document.getElementById('mydiv').style.width= '200px';
      setTimeout(function(){document.getElementById('mydiv').style.width= '200px';},1000);
    }
  </script>
</head>
<body>
  <div id='mydiv'></div>
</body>
</html>
```

We fisrt define a object in style. It is a black square. Then it can be chosen in body part to be shown by div id identification. Later it can be chosen to be controlled by script command such as we can define its style after a definite time we set.
