

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
			background: pink;
			list-style: none;
			border:1px solid red;
			margin-top:3px;
			text-align:center;
		}
		a{
			text-decoration: none;
			line-height:50px;
			
		}
	</style>
</head>
<body>
	<ul id="ul">
		<li>1</li>
		<li>2</li>
		<li>3</li>
		<li>4</li>
		<li>5</li>
	</ul>
	<script>
		window.onload = function(){
			/*
				找到某个元素的下个兄弟节点:nextElementSibling

				找到某个元素的下个兄弟节点:previousElementSibling

			*/

			var ul = document.getElementById("ul");
			var lis = ul.children;
			lis[0].nextElementSibling.style.background="red";
			lis[0].nextElementSibling.nextElementSibling.style.background="purple";
			lis[1].previousElementSibling.style.background="yellow";

			console.log(lis[0].nextElementSibling.nextElementSibling)
		}
	</script>
</body>
</html>
```
![这里写图片描述](http://upload-images.jianshu.io/upload_images/6636198-327224a5e4795c8c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



