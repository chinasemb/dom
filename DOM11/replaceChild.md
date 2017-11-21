

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#div1{width: 300px;height: 300px;background-color: pink}
		#div2{width: 300px;height: 300px;background-color: purple}
	</style>
</head>
<body>
	<div id="box">
		<input type="button" value="点击替换" id="btn">
		<div id="div1"></div>
		<hr>
		<div id="div2"></div>
	</div>
	<script>
		/*需求:
			当点击按钮的时候,将粉色方块替换成紫色方块;

			父级.replaceChild(替换成的最终颜色,被替换的颜色)
		*/

		var btn = document.getElementById("btn");
		var pink = document.getElementById("div1");
		var purple = document.getElementById("div2");
		var box = document.getElementById("box");

		btn.onclick = function(){

			box.replaceChild(purple,pink);
		}
	</script>
</body>
</html>
```

