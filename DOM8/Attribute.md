

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
		var div1 = document.getElementById('div1');
		div1.index = 1 ;
		alert(div1.id);
		alert(div1["id"]);
		/*获取元素行间的属性 (专门操作行间样式的)*/
		div1.setAttribute("index","3");
		alert(div1.getAttribute("id"));
		
		/*给元素设置添加属性 键值对 */
		alert("下面就删除了");
		div1.removeAttribute("index");
		alert(div1.getAttribute("index"));

		/*可以操作行间的自定义属性
			可以获取src,href等的相对地址.
		*/
		console.log(img.getAttribute("src"));

		if(img.getAttribute("src") == "../../s.png"){
			alert("真");
		}else{
			alert("假");
		}
	</script>
</body>
</html>
```

