```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#ul li{
			width: 150px;
			height: 50px;
			background: blue;
			list-style: none;
		}
	</style>
</head>
<body>
	<ul id="ul">
		<li>11</li>
		<li>22</li>
		<li>33</li>
		<li>44</li>
		<li>55</li>
	</ul>
	<script>
		/*
		parenNode:
			查找某个元素的父节点.
		*/
		var ul = document.getElementById("ul");
		var alis = ul.children;

		//console.log(alis[0].innerHTML);
		console.log(alis[0].parentNode.parentNode.parentNode.parentNode.parentNode);
	</script>
</body>
</html>
```
![这里写图片描述](http://upload-images.jianshu.io/upload_images/6636198-0c7a701a25dede76.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![这里写图片描述](http://upload-images.jianshu.io/upload_images/6636198-b31e1e8c3c1cb15e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)