

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<input type="button" value="点击删除" id = "btn">
	<ul id="ul" >
		<li>1</li>
		<li>2</li>
		<li>3</li>
	</ul>
	<script>
		/*
			删除节点:
				父级.removeChild(指定的子节点)
			注意:
				如果指定的子节点没有,会报错.(进行判断解决)
		*/
		var ul  = document.getElementById("ul");
		var num = 0;

		var btn = document.getElementById("btn");

		btn.onclick = function(){
			if(ul.lastElementChild){
				ul.removeChild(ul.lastElementChild);
			}
			
		}
	</script>
</body>
</html>
```

