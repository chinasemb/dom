

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		div{padding:100px;}
		#div1{background-color: #FFF5EE;position:relative;}
		#div2{background-color: #F4F4F4;}
		#div3{background-color: #C1FFC1;position:relative;}
	</style>
</head>
<body>
	<div id="div1">
		<div id="div2">
			<div id="div3">
				
			</div>
		</div>
	</div>
	<script>
		/*offsetParent  最近的有定位属性的祖先节点*/
		var div3 = document.getElementById("div3");
		console.log(div3.offsetParent);
		/*结果导向证明,div3的最近的有定位属性的祖先节点是body;
			当div1和div3都有定位的时候,div3的offsetParent是idv1
			如果祖先节点都没有定位,默认为body,子元素和父元素都有定位,而且其他浏览器为了兼容,div还要有宽高.
		*/
	</script>
</body>
</html>
```

