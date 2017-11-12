

	>document:9
	>3文本节点:    数字,文本,换行.
	
	>8注释节点
	
	>2属性节点  div.attributes[0]    nodeValue 查看 节点的属性值  
					nodeName查看属性名

----------

>1元素节点
>childNodes:获取某个节点下的子节点

----------
children:找到某个元素下面的所有元素子节点  

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#ul li{
			width: 30px;
			height: 30px;
			background: yellow;
			list-style:none;
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
			var ul = document.getElementById("ul");
			var lis = ul.childNodes;
			// var lis = ul.children;

			document.onclick = function(){
				for(var i=0; i<lis.length; i++ ){
					if(lis[i].nodeType===1){
						lis[i].style.width="140px";
					}
					
				}
				
			}
		}
	</script>
</body>
</html>
```

