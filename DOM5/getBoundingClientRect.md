

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{margin:0;padding:0;}
		#div1{background-color: #FFF5EE;position:relative;width: 200px;height: 200px;left:30px;top:30px; border:3px solid #7D26CD;}
		#div2{background-color: #FF7F00;position:relative;width: 100px;height:100px;left:30px;top:30px; border:3px solid #7D26CD;}
		#div3{background-color: #C1FFC1;
			position:absolute;
			width: 50px;
			height: 50px;top:20px;
			 border:3px solid #7D26CD;
			 left:0;/*important*/
			 transition:1s left;}
	</style>
</head>
<body>
	<input id = "btn" type="button" value = "点击移动">
	<div id="div1">
		<div id="div2">
			<div id="div3">
				
			</div>
		</div>
	</div>
	<script>
		/*offsetLeft  左外边框到最近的有定位父级的左内边框的距离*/
		/*offsetTop  上外边框到最近的有定位父级的上内边框的距离*/
		/*offsetRight offsetBottom 是没有的*/
		var div3 = document.getElementById("div3");
		console.log(div3.offsetParent);
		console.log(getComputedStyle(div3).left);/*20px*/
		console.log(div3.offsetLeft);
		console.log(div3.offsetTop);/*20*/
		/*如果子元素和父级元素都没有定位的话,offsetLeft是8px,取消margin和padding之后,是0px*/

		/*需求:当点击按钮的时候,div3移动到左顶边*/
		var btn = document.getElementById("btn");

		btn.onclick = function(){
			
				div3.style.left=-div3.getBoundingClientRect().left+"px";
				/*
					getBoundingVlientRect : 返回值为一个对象,获取某个元素的信息(高版本:left,right,top,bottom,width,height)
					距离可视区屏幕的上下左右的距离.
				*/
				
			}
			
		


	</script>
</body>
</html>
```

