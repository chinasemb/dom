

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
			var left = 0;
			var elem = div3;
			var div3B = parseInt(getComputedStyle(div3).borderLeftWidth);
			while(elem){//如果有elem这个元素,就会走这个循环
				left+=elem.offsetLeft+parseInt(getComputedStyle(elem).borderLeftWidth);
				elem=elem.offsetParent;//第一次计算之后elem就会由div3变成div2
				
			}
			left -= div3B;
			div3.style.left=-left+"px";
			console.log(left);
		}


	</script>
</body>
</html>
```

