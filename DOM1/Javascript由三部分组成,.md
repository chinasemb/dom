Javascript由三部分组成,

 1. ECMAscript(javascript核心标准,也是一个解析器,是一个规范)
 2. DOM (通过document提供的一些属性或者方法来操作页面,帮助我们去操作页面的结构,添加删除某个标签,document提供了一些接口,赋予开发者操作页面的能力)
 3. BOM (通过window提供的一些属性和方法来操作浏览器,更加方便的区操作浏览器,拉到底部,有数据加载)

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<div id="div1"></div>

	<script>
		window.onload = function(){

			var oDiv = document.getElementById("div1");
			oDiv.style.cssText = "width:100px;height:100px;background:yellow;" 
		}
	</script>
</body>
</html>
```
![这里写图片描述](http://upload-images.jianshu.io/upload_images/6636198-b6063945d36295f7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
按照节点的类型划分:
​	
nodeType 
 1. 元素节点:1 


```
 <!doctype html>
 <html lang="en">
 <head>
 	<meta charset="UTF-8">
 	<title>Document</title>
 </head>
 <body>
 	<div id="div1">
 		
 	</div>
 	<script>
 		window.onload = function (){

 			var oDiv = document.getElementById("div1");
 			console.log(oDiv.nodeType);
 		}
 	</script>
 </body>
 </html>
```