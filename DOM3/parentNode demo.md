

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
	<ul id= "ul">
		<li><a href="javascript:">隐藏1</a></li>
		<li><a href="javascript:">隐藏2</a></li>
		<li><a href="javascript:">隐藏3</a></li>
		<li><a href="javascript:">隐藏4</a></li>
		<li><a href="javascript:">隐藏5</a></li>
	</ul>
	<script>
		window.onload=function(){
			var a = document.getElementsByTagName("a");

			for(var i=0;i<a.length;i++){
				a[i].onclick=function(){
					this.parentNode.style.display="none";
				}
			}
		}
	</script>
</body>
</html>
```
![这里写图片描述](http://upload-images.jianshu.io/upload_images/6636198-49b4ae8f632fbdfa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![这里写图片描述](http://upload-images.jianshu.io/upload_images/6636198-af0d692c12bba65a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

