<!doctype html>
<html lang="en">
<head>

	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		
	</style>
</head>
<body>
	<input type="button" id = "btn" name = "" value = "点击添加">

	<ul id="ul">
		<li>0</li>
	</ul>
	<script>
		/*
			插入元素:(向父级末尾添加一个元素)
				ParentNode.appendChild(childNode)
	
			插入元素:(向父级中的某个元素前插入一个元素)
				ParentNode.insertBerore(新添加的元素,原来的元素)
	
			特性: 如果第二个参数为假的,那么会将某个元素添加到父元素的末位.
		*/
		var btn = document.getElementById("btn");
		var ul = document.getElementById("ul");
	
		var num  = 0 ;
		btn.onclick = function(){
			num++;
			var li = document.createElement("li");
	
			li.innerHTML = num;
			console.log(ul.children[0]);
			ul.insertBefore(li,ul.children[0]); //在ul的第一个子节点前插入元素
		} 
	</script>
</body>
</html>